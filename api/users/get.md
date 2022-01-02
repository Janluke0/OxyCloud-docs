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
## Flow
![flow](https://www.plantuml.com/plantuml/png/VLB1Yjim4BtxAsQXq1JYY5n3MpPDmZQmqANkihU28etj0LdoIgEuwQ7VNibssqlIYqSpVk-DtaFtWQNds9dYJcDD5c7xKZsb7bhcFco4y79ODSHjFCM0NZdBQ7cbN2Va48myXLnBIZz2MJjVzaRQB2ZEw_LgBJG5Bkx8AXCrHc_-w8jKTwxhd5trUNtn5fwjIeEa3jmYrCuODv1jmEHhiGFbKJ92eAutL1DgE1CEjyIhlx1vmJNS0rhqqeZdP6s4NLVhavAIJCuUBMFZnwFOFXqV9ECWBxUf5QheYIz7ZPPJJPQJbhGAnSurbjZTvcPiP1IFiZjf-PyTxBniK8oESUugz6TIU9krbonFCg3ONwpitFxJ79F1cdFQdfgMGPD7bTqMHSve4TDd2Tl8hVFq4pLCWr_lYdzfBD9n2Lz-N7R6HGrZbm2ptuMQwXBcmIW1lNDcX1LZ-xuiFsRc1Zo-Hl8OHbY0eINL0dQI38nlDus8MtZpccymyUOD6wWEZuVTDo2zd0WldmzV3nFv-uV4AExHwkJwDm00)