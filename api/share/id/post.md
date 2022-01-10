# OxyCloud API
## Share a document with a user

**URL**: `/share/:id`

**Method**: `POST`

**Auth required**: YES

### Request
#### Params
|name         |description                       |type   |source   |default|required|
|-------------|----------------------------------|-------|---------|-------|--------|
|id           |the document id                   |string |url parms|       | yes    |
|share_email  |the user to who share the doc     |string |query par|       | yes    |

### Response
#### Scheme
*success:*
```json
{}
```
*error:*
```json
{
    "message": string,
}
```

#### Example
```json
{}
```
