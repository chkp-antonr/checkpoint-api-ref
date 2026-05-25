# add-resource-mms

**Collection:** Web API (version 2.0.1) > 43 Resource MMS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-resource-mms`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newMmsResource"
}
```

## Example Responses

### Example 1: add-resource-mms
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7cc26aa9-170b-44cc-9a12-0712bd2c2220",
  "name": "newMmsResource",
  "type": "resource-mms",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1744107474093,
      "iso-8601": "2025-04-08T13:17+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1744107474093,
      "iso-8601": "2025-04-08T13:17+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "track": "none",
  "action": "accept"
}
```
