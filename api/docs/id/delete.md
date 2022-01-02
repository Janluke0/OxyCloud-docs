# OxyCloud API
## Delete a document

Given the file-id, if the file exist and the user is the owner, move the file to the trash if *delete* (et viceversa) and delete it permanently if *doom*

**URL**: `/docs/{id}`

**Method**: `DELETE`

**Auth required**: YES

### Request
#### Params
|name   |description  |type   |source   |default |required|
|-------|-------------|-------|---------|--------|--------|
|id     |the file id  | string|path parm|        | yes    |
|delete |mv to trash? |   bool| url parm| false  | no     |
|doom   |dl permantly?|   bool| url parm| false  | no     |

### Response
**THIS IS HOW IT SHOULD BE ===> FIXME**
#### Scheme
*success:*
```
{}
```
*error:*
```json
{
    "message": string,
}
```

#### Example
```
{}
```
