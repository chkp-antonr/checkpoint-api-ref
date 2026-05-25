# add-data-type-group

**Collection:** Web API (version 2.0.1) > 51 Data Type Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-type-group`

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
  "description": "add data type group object",
  "file-type.1": "file-attr-obj"
}
```

## Example Responses

### Example 1: add-data-type-group
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
      "posix": 1695716698680,
      "iso-8601": "2023-09-26T11:24+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695716698680,
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
      "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
      "name": "Any",
      "type": "CpmiAnyObject",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "General/globalsAny",
      "color": "black"
    }
  ]
}
```
