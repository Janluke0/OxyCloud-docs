# OxyCloud API
## Download a document

Given the file-id, if the file exist and the user is authorized to access to it, returns a s3 presigned url that can be used to download the files

**URL**: `/docs/{id}`

**Method**: `GET`

**Auth required**: YES

### Request
#### Params
|name   |description|type   |source   |default |required|
|-------|-----------|-------|---------|--------|--------|
|id     |the file id| string|path parm|        | yes    |

### Response
**THIS IS HOW IT SHOULD BE ===> FIXME**
#### Scheme
*success:*
```json
{
    "url":string
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
    "url":"https://[BUCKET_NAME].s3.amazonaws.com/[OBJ_ID]?AWSAccessKeyId=XXX&Signature=XXX&x-amz-security-token=XXX&Expires=XXX"
}
```