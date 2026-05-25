# add-data-type-compound-group

**Collection:** Web API (version 2.1) > 59 Data Type Compound Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-type-compound-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "compound-group-obj",
  "description": "Compound group object",
  "matched-groups.1": "trad-group-obj",
  "unmatched-groups.1": "keywords_obj"
}
```

## Example Responses

### Example 1: add-data-type-compound-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "eff8261a-92a8-46a2-85d3-f5242f176c31",
  "name": "compound-group-obj",
  "type": "data-type-compound-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695814969156,
      "iso-8601": "2023-09-27T14:42+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695814969156,
      "iso-8601": "2023-09-27T14:42+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "Compound group object",
  "matched-groups": [
    {
      "uid": "be7f94fb-1a57-46a5-938e-ca557d816bf4",
      "name": "trad-group-obj",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    }
  ],
  "unmatched-groups": [
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
