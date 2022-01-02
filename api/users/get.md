# OxyCloud API

## Search user by email

Given the begin of the email return all users that match

**URL**: `/users`

**Method**: `GET`

**Auth required**: YES

### Request
#### Params
|name     |description  |type   |source   |default |required|
|---------|-------------|-------|---------|--------|--------|
|q        |the query    | string| url parm|        | yes    |

### Response
#### Scheme
*success:*
```json
[]File
```
*error:*
```json
{
    "message": string,
}
```

#### Example
```json
[
    {
        "id":"c6c94228-7f5c-4dba-98de-7f27f0e97e95",
        "email":"janluke@mail.com",
    },
    {
        "id":"84abbe84-9e6e-47cb-810f-f6bceedd28f3",
        "email":"giovanni.rana@mail.com",
    }
]
```
