# set-data-type-group

**Collection:** Web API (version 2.1) > 58 Data Type Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-type-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "data-group-obj",
  "file-content.1": "keywords_obj"
}
```

## Example Responses

### Example 1: set-data-type-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f5ecc9e0-eb32-4beb-bd47-f917eb57828f",
  "name": "data-group-obj",
  "type": "data-type-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695717571065,
      "iso-8601": "2023-09-26T11:39+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695716698776,
      "iso-8601": "2023-09-26T11:24+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "add data type group object",
  "file-type": [
    {
      "uid": "2bafa11d-b388-4287-8994-c48c657e6d05",
      "name": "file-attr-obj",
      "type": "data-type-file-attributes",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    }
  ],
  "file-content": [
    {
      "uid": "8692b78b-e668-47c6-a87f-99ffbf659b74",
      "name": "keywords_obj",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    }
  ]
}
```
