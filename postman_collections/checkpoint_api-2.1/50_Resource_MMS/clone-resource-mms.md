# clone-resource-mms

**Collection:** Web API (version 2.1) > 50 Resource MMS
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-resource-mms`

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

### Example 1: clone-resource-mms
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ee4f31b4-872b-4426-a375-99a1a4fa824e",
  "name": "newMmsResource_Clone",
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
      "posix": 1744109755237,
      "iso-8601": "2025-04-08T13:55+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1744109755237,
      "iso-8601": "2025-04-08T13:55+0300"
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
