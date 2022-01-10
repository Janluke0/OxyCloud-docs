# OxyCloud API
## Unshare document
Unshare a document previously shared with a certain user, by email

**URL**: `/share/:id`

**Method**: `DELETE`

**Auth required**: YES

### Request
#### Params
|name         |description                       |type   |source   |default|required|
|-------------|----------------------------------|-------|---------|-------|--------|
|id           |the document id                   |string |url parms|       | yes    |
|unshare_email|the user from which remove sharing|string |query par|       | yes    |

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
