# OxyCloud API
## Delete a document

Given the file-id, if the file exist and the user is the owner, move the file to the trash if *delete* (et viceversa) and delete it permanently if *doom*

**URL**: `/docs/{id}`

**Method**: `DELETE`

**Auth required**: YES

### Request
#### Params
|name   |description  |type   |source   |default |required|
|-------|-------------|-------|---------|--------|--------|
|id     |the file id  | string|path parm|        | yes    |
|delete |mv to trash? |   bool| url parm| false  | no     |
|doom   |dl permantly?|   bool| url parm| false  | no     |

### Response
#### Scheme
*success:*
```
{}
```
*error:*
```json
{
    "message": string,
}
```

#### Example
```
{}
```
## Flow
![flow](https://www.plantuml.com/plantuml/png/ZL9TJzjA47tthnWG4hcI4yEh1LTm4yIDT0Ne1if3LLLhxyJUThrZxSucJH7zxVNw8q19ghxix7XdpZbpnXUEXMLVwUX0ub8PXCl7nLsJGybSkpH9h5XF2iMbpxn3cvDXD3p9gKh4sccHkH37gdbmuoNPSQs52O39wlHqSff8vJWwK2RNNgAtUi1FcZYbgY8pgGDzT0mFfa6jq31mYR0ahMcjJ04wo6A2tA9W1AUgMgkbGWahXUjzu8jjMKUmi-uQ3LgXamU7jYtRZLOtIBbWHMPk60lRNfFBk_crO5oBpVxM1URUAjxC9HfkufI2Ac5oJAPK6CMqlpVKUiRaFr5bKlo6WycA0fDsOkop1TgLod5_rqomo8J3PBOnegBPFxrD6fSStBQgA1caifY7QQCeU3JopH73fUUIhFgE4heFF_wANjmODTSORhzjffgyX925We5dj5GQtMUPnN3OYuL1p67y3kba1zIkIKUkIsCOG3EVVqKEY9s38p8peYg6S49G4SFBew-bO9oMIaiNmqERGHvIYmOaQWmsW6F1thMDKPWTnkE_WwuKAbgX0qcvx_vX0hR2bJ0Ys_xGLDVa56Cx89o5li6951PNzw2QQw11UNxKNM1-StyBd6bu_FVg_wlMxFEZSAh6Z9iPgAPKoUYjb9CKQhILC6XORw276eH5eM8VFL4Ls4FyO-u1fQNlB6u0sQ9eujCDhZy8xJ5zskAdR3q-FqTTRTlMxow5MIUMiY-OSnGTtrcgHI4OVzq0C6styrR2wqM-4Z8jXIbGjc9S-d6h9dxb-wSONiGkIKkqWzWjnTbxZclahHOGHlRFOUlA3dg5w_DQMCmuka0ZVQL_0W00)
