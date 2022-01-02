# OxyCloud API
## List own documents
Given a folderid (or an empty string for the root) it returns a list of its content

**URL**: `/docs`

**Method**: `GET`

**Auth required**: YES

### Request
#### Params
|name   |description              |type   |source   |default|required|
|-------|-------------------------|-------|---------|-------|--------|
|deleted|filter by deletion status|bool   |url parms|*false*| no     |
|folder |the parent folder        |string |url parms| *""*  | no     |

### Response
#### Scheme
*success:*
```json
{
    "files": []File,
    "folders": []Folder,
}
```
*error:*
```json
{
    "message": string,
}
```

#### Example
```json
{
 "files": [
    {
        "id":"3dd4d7a7-3f90-43e2-817b-13458cdb7b59",
        "size":105529,
        "owner":"c6c94228-7f5c-4dba-98de-7f27f0e97e95",
        "last_edit":"2021-12-28T12:05:33.715Z",
        "etag":"916b10636363bc39c431e758cb9b45c9",
        "folder":"",
        "shared_with":[],
        "name":"testfile.zip"
    }
],
 "folders": [
    {
        "id":"3dd4d7a7-3f90-43e2-817b-13458cdb7b59",
        "owner":"c6c94228-7f5c-4dba-98de-7f27f0e97e95",
        "name":"testDir"
    }
 ]
}

```