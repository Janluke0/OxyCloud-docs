# OxyCloud API

The OxyCloud API is the main entrypoint for the Oxycloud application. The API is built using **AWS API Gateway** which provides multiple useful features that we employed in the project. 

Every endpoint of the API is either a *AWS Lambda* integration or a more general *AWS Service* integration. We tried as much as we could to avoid creating Lambda functions that provide functionalities that can be obtained just by integrating the services directly with *API Gateway*.<br>
This fulfils two important objectives:
- **Cost reduction**: Even if the Lambda cost can be very small, it is still a voice in the final infrastructure cost that can be easily avoided by integrating services directly without the help of the Lambda function.
- **Infrastructure management hassle reduction**: One less piece of infrastructure to maintain is one problem less to deal with.

Another important feature that we used in the project was the integrated authorization mechanism. We initially went for a *IAM authorization* mechanism to implement *role-based* access to the API. In reality, we didn't need endpoint-level user access control because, at least in this first instance of the app, we don't have multiple roles and every user can access each method in the API. This led us to change the authorization mechanism to a *Cognito User Pool authorization* which was more than enough for our purposes and let us get rid of the *Cognito Identity Pool* that we were using to assume IAM roles and give credentials to our *User Pool* users to access the OxyCloud API. In any case, in future instances of the app we can quickly change that and restrict User access at the single endpoint level.  

## Methods

|name                             |path         |method  |
|---------------------------------|-------------|--------|
|[listDocs](docs/get.md)          |`/docs`      |GET     |
|[uploadDoc](docs/put.md)         |`/docs`      |PUT     |
|[downloadDoc](docs/id/get.md)    |`/docs/:id`  |GET     |
|[renameDoc](docs/id/post.md)     |`/docs/:id`  |POST    |
|[deleteDoc](docs/id/delete.md)   |`/docs/:id`  |DELETE  |
|                                                        |
|[listShared](share/get.md)       |`/share`     |GET     |
|[shareDoc](share/id/post.md)     |`/share/:id` |POST    |
|[UnshareDoc](share/id/delete.md) |`/share/:id` |DELETE  |
|                                                        |
|[searchUsers](users/get.md)      |`/users`     |GET     |
|[getUser](users/id/get.md)       |`/users/:id` |GET     |

## Entities

### File
|name       |description            |    type|
|-----------|-----------------------|--------|
|id         |the unique id          |    uuid|
|size       |size in bytes          |     int|
|owner      |the owner id           |    uuid|
|last_edit  |timestamp              |datetime|
|etag       |given  by s3           |  string|
|folder     |the parent id          |    uuid|
|shared_with|users which have access|  []uuid|
|name       |the filename           |  string|

### Folder
|name       |description            |    type|
|-----------|-----------------------|--------|
|id         |the unique id          |    uuid|
|owner      |the owner id           |    uuid|
|folder     |the parent id          |    uuid|
|name       |the filename           |  string|

### User
|name       |description            |    type|
|-----------|-----------------------|--------|
|id         |the unique id          |    uuid|
|email      |the user's mail        |  string|

### Authorization

Tokens are obtained from cognito endpoint using the supplied `client_id` and the `USER_PASSWORD_AUTH` and `REFRESH_TOKEN_AUTH` *AuthFlow* of the `InitAuth` method.

*Identity token* must be included in the `Authorization` header of the requests where authorization is required.