# OxyCloud API

## Rename a document

Given the file-id, if the file exist and the user is the owner, rename the file

**URL**: `/docs/{id}`

**Method**: `POST`

**Auth required**: YES

### Request
#### Params
|name     |description  |type   |source   |default |required|
|---------|-------------|-------|---------|--------|--------|
|id       |the file id  | string|path parm|        | yes    |
|filename |new file name| string| url parm|        | yes    |

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
![flow](https://www.plantuml.com/plantuml/png/VL3DRjim3BxxATWYm38WYP1hi0pDag0BCBJ5tAB7GPPecu0i6H8LBplisITvoNPfUX59-_lvoBl0qdFiJ76ZiIQBi7ajdz8CBNCVLa9uEImQuZPMCQ1NpZ9QNYZN2Ja48wkGwvpIZp2ldP_tHjeiA8xBvM8fD0KkRiWg4pL6Roxw8jMjwpfd5tssBpx0Yqsg7Le6RX5gPumRo3PWSYnse3nAHWZKzOPgGWr7mk6QUFaFTZPu2tUF5hqquYMW7s5lg_L9IKacPm-MiV5ZApPFXtl9ECZJTMg9AdhYqq6ZvLItBgUILg7OkiOIk-lSZ8sCufliAYtVyM3dPODYt1ZFKud-I0glitQIPIK3Yjt9oixjlfpFPB3cV6rFJSkWoQFAsnP5lj4qfcS6cyYjy_GBDVpzyFjZyVyQqzJEuF7dQMjSr92d3BZuJ6io67xeQWQtvx1m2NCxIy0YQy9y_ZbJL-0nyJ201ErKxD1oze9F6N2HMa6vVnwdZ5rFB0wvWSF3yoDmPU3rw_xxVWoxdkINKgw77UZrX7HnXrQdtVy0)
