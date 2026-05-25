# set-data-type-file-attributes

**Collection:** Web API (version 2.1) > 54 Data Type File Attributes
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-type-file-attributes`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "file-attr-obj",
  "file-groups-list.1": "Word",
  "match-by-file-size": false
}
```

## Example Responses

### Example 1: set-data-type-file-attributes
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b3f18062-57c4-43f9-b3d4-6aed11c8c688",
  "name": "file-attr-obj",
  "type": "data-type-file-attributes",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695670957280,
      "iso-8601": "2023-09-25T22:42+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695670212542,
      "iso-8601": "2023-09-25T22:30+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "match-by-file-size": false,
  "match-by-file-name": true,
  "match-by-file-type": true,
  "file-name-contains": "expression",
  "file-groups-list": [
    {
      "uid": "ad38c839-f2eb-4d2b-bd31-6f80ded598bb",
      "name": "Word",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/word_group",
      "color": "black"
    }
  ]
}
```
