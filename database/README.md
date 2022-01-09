# Database

In order to reduce the number of calls to the S3 storage bucket to list the User's files a DynamoDB table was created to collect User's files' metadata.

Keeping in mind the same idea to optimize the number of *scans* performed by DynamoDB to retrieve records, we designed the table so that the primary key in the DB is the *user_id*. In fact, knowing that the mostly performed action by the users is LIST, using *user_id* as the primary key, let us retrieve users' data just by performing the *query* DynamoDB action which does not cycle thorugh the entire DB, but looks only at records having the provided index. 

A *file_id* is also provided to further narrow down the search space when a GET request on a specific file is performed by the client (download file, delete file, rename file ...).