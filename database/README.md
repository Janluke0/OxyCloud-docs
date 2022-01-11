# Database

In order to reduce the number of calls to the S3 storage bucket to list the User's files a DynamoDB table was created to collect User's files' metadata.

Keeping in mind the same idea to optimize the number of *scans* performed by DynamoDB to retrieve records, we designed the table so that the primary key in the DB is the *user_id*. In fact, knowing that the mostly performed action by the users is LIST, using *user_id* as the primary key, let us retrieve users' data just by performing the *query* DynamoDB action which does not cycle thorugh the entire DB, but looks only at records having the provided index. 

A *file_id* is also provided to further narrow down the search space when a GET request on a specific file is performed by the client (download file, delete file, rename file ...).

Events are published on a DynamoDB stream and some of them are used as triggers for specific Lambda functions.
For instance, the *doomFile* Lambda function, which is used to delete a file or a folder from the storage bucket, is invoked as the *is_doomed* attribute is updated in the corresponding file/folder record in the *User files* table.
Basically, as the *is_doomed* attribute is set to true, the file gets deleted from the S3 bucket.

A complementary *Users* table was also created to keep information about Users' *subscription plans* and *companies*.
In the first place we planned to use only the **Cognito User Pool** as the primary database for user data, however as some business-logic related issues came into existence we decided to introduce this auxiliary DynamoDB table.
One of the main problems we were facing was the fact that the *subscription_plan* should have been a **read only** attribute for the client and that conflicted with our original design of the *sign up* procedure. The *Users* table introduction helped us solve the issue.