# OxyCloud API

## Rename a document

Given the file-id, if the file exist and the user is the owner, rename the file

**URL**: `/docs/{id}`

**Method**: `POST`

**Auth required**: YES

### Request
#### Params
|name     |description  |type   |source   |default |required|
|---------|-------------|-------|---------|--------|--------|
|id       |the file id  | string|path parm|        | yes    |
|filename |new file name| string| url parm|        | yes    |

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
