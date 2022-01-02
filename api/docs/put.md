# OxyCloud API
## Upload a document

Generate a presigned form to be used to upload the file directly on the returned s3 bucket

**URL**: `/docs`

**Method**: `PUT`

**Auth required**: YES

### Request
#### Params
|name   |description|type   |source   |default |required|
|-------|-----------|-------|---------|--------|--------|

### Response
#### Scheme
*success:*
```json
{
  "url": string,
  "fields": Map<string,string>
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
  "url": "https://[BUCKET_NAME].s3.amazonaws.com/",
  "fields": {
    "x-amz-meta-displayname": "[base64(filename)]",
    "x-amz-meta-folder": "[FOLDER_ID]",
    "x-amz-meta-user": "[USER_ID]",
    "key": "[FILE_ID]",
    "x-amz-algorithm": "XXX",
    "x-amz-credential": "XXX",
    "x-amz-date": "XXXX",
    "x-amz-security-token": "XXX",
    "policy": "XXX",
    "x-amz-signature": "XXX"
  }
}
```
