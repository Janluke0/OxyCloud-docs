# OxyCloud API
## Get user

Given the id it returns the User entity

**URL**: `/users/{ID}`

**Method**: `GET`

**Auth required**: YES

### Request
#### Params
|name     |description  |type   |source   |default |required|
|---------|-------------|-------|---------|--------|--------|
|id       |the user   id| string|path parm|        | yes    |

### Response
#### Scheme
*success:*
```json
User
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
    "id":"c6c94228-7f5c-4dba-98de-7f27f0e97e95",
    "email":"janluke@mail.com",
}
```
## Flow
![flow](https://www.plantuml.com/plantuml/png/VP31Rjiy383lVWeM-84_0v88kGRRq2m9kW05LYmhUbOasYOWInv5nSiEU_P9ZhjTcbrCaVxu4UHz5CsIEbVTMQp98snUZayvXrQaZskbM0_BXgHDfnIHJV22NfOcT4eFqUbJB751-KTSr84NlTE-2DLvjLgkbAKerHrvuvB5nExLhtBSXguBVjcNyTN_yEopjSjsa1QX3iw5WNm3ZZo2132CMX0YTRsZcj32cN2u9J_-mQO1Rt4Fw96rKyyHUSJUjlNPPBHGy0SlsF3uL9kdmuCM7FJbTkiHJMAIoy6YbnppojcblK6r3Oqd2RTx2vi4rQFkJbR_OuO4rWsgSMESiYFocGpUxjffqISTKUqkNdTXzsawayDQohMPcbR04gCfsrPLkT4ivSySDadQmFGJBLmBlzvLVwynoyyvVFbnsRgGB9Ii0DE-CtEDSvWAemBw4Do8LMEwM7miZMjW_9w8CLwfWQI5_yYMQV2-G9Dj3SVzutxx3SZEiTFauENp_ki-fnyoFZeB_-gKn3v2JHm50WCo1wxkqTjyWjy0)
