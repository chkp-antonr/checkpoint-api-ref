# set-data-type-traditional-group

**Collection:** Web API (version 2.1) > 57 Data Type Traditional Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-type-traditional-group`

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
  "data-types.1": "keywords_obj"
}
```

## Example Responses

### Example 1: set-data-type-traditional-group
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
      "posix": 1695709375855,
      "iso-8601": "2023-09-26T09:22+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695708713261,
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
