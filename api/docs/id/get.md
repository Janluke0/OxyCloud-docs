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

## Flow
![flow](https://www.plantuml.com/plantuml/png/VL71RXen4BtlLqoYIANLWfKh8YWKQ8gKDb4eog6gAgyzkrZrsbjxp8OU-ksrMQ2D1BsiFUFtthmtU-k9EmgrpYuabieWJ9wNZx66DL7ZXumvtWugHUjG18zEM4DeQ21ipNZhDIzyEligFlX-QLs_qTmaGRQvlXvSCwayPHVA21qa1gSF-YoUKrlNrWoQD3vx0oiZOYEg0wqHIgkrRPMfG2TRP44uv8JWLTreLIgKi57OdXDV7c7TW9EuEpJek6Qh6As3dLHhefBWfAnP6CBAxQviyhYuuuGjtvwdBb44fsYxa6WedbERN74Za4rjPHJPyzo43OJidjU5vF-PGTRn2jakCUwh9RgD4dYUDUF42-wHpRQ6rtRsleDgB2ajswbgJI2LGv72Pcb3lH0_EKm2hQrJlr12r_ZzDlkxYrwyvl3mifrg6oIaAW4EKtgbqkY_ooA7oxrLE5Yvp2EmIzkhqCniQxJbSkLq3jsV8WIvxq8CirC-5RldkpA7mumYY1z8EqAMNCEetnydTqDm-3CeXpx5FghpU1MXHaCfMuT-xMa8NqTgt3ZxiXqnDVwMlNxkA8UqGrZEx-VJB_0EFZmzV08gD3n_d3_DGScRAnNtz7a6aOpkvYhP-zVaFiiG6dIbTRK_kinkqSXGwpy0)