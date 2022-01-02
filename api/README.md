# OxyCloud API

## Methods

|name                             |path         |method  |
|---------------------------------|-------------|--------|
|[listDocs](docs/get.md)          |`/docs`      |GET     |
|[uploadDoc](docs/put.md)         |`/docs`      |PUT     |
|[downloadDoc](docs/id/get.md)    |`/docs/:id`  |GET     |
|[renameDoc](docs/id/post.md)     |`/docs/:id`  |POST    |
|[deleteDoc](docs/id/delete.md)   |`/docs/:id`  |DELETE  |
|
|[listShared](share/get.md)       |`/share`     |GET     |
|[shareDoc](share/id/post.md)     |`/share/:id` |POST    |
|[UnshareDoc](share/id/delete.md) |`/share/:id` |DELETE  |
|
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