# add-data-type-traditional-group

**Collection:** Web API (version 2.1) > 57 Data Type Traditional Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-type-traditional-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "trad-group-obj",
  "description": "traditional group object",
  "data-types.1": "weighted-words-obj",
  "data-types.2": "file-attr-obj"
}
```

## Example Responses

### Example 1: add-data-type-traditional-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "be7f94fb-1a57-46a5-938e-ca557d816bf4",
  "name": "trad-group-obj",
  "type": "data-type-traditional-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695708713203,
      "iso-8601": "2023-09-26T09:11+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695708713203,
      "iso-8601": "2023-09-26T09:11+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "traditional group object",
  "data-types": [
    {
      "uid": "34f9eae1-0bc3-43ae-b3cb-24f11cb32d9a",
      "name": "weighted-words-obj",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
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
  ]
}
```
