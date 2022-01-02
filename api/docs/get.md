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
## Flow
![flow](https://www.plantuml.com/plantuml/png/VLBDRXCn4BxlKqohIXIKnCeregWX2ILIeLL3rIFoshEx8tdjnHvd2GUU7JkxWKl3QNxy_On7SnjOUewjAIuqLcGHbY-xnrH3mzo5XH1UzhEQk8bb3EYLiuoMPygrGlR1o3BaEANq4AQLyzFEI9i5nNu-dys5fi351LbbeiRepKbVfBXoRUlihClsnHjujYerq39mWr0vOrnFjWQJns87ogDaX41jPwWYrB0dxC-9x_x2HeFNS7TeqKiZdWFw0VQgMfUKb6HoTciPQtzCnV9nUoSPUtauJzsXYfxuiDLeESMLorD9gr2iN6s9tNbknaP6SI_RKil_UB3piaPn_36ErGxzdXIUPwqbor865Ek3bQrRVnoW1YlEo_PKDmoQFAhysI9lw3fVm0IMaHldwHTg61g_tnR_Td6TqWay_3oiZ8iQSfK19vVhYWo6xxgSmEKuAfn6kPmaO94ruVrq-Y5p5-3nHoIFuNWKu_c1gq3c2z7ei_K0FoalOBUvtwo-mJluzFJm1RWqyF9vyxGP6JTNGuJbrpMutkPE36DDIG4DCkgRgp4fRj7gj9i_)