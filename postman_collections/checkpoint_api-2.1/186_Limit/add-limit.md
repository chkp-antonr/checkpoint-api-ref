# add-limit

**Collection:** Web API (version 2.1) > 186 Limit
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-limit`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "limit_obj",
  "enable-download": "true",
  "download-unit": "Gbps",
  "download-rate": "3"
}
```

## Example Responses

### Example 1: add-limit
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "769f6211-c8dc-4e79-8fe4-3842e5031c22",
  "name": "limit_obj",
  "type": "limit",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1676810586312,
      "iso-8601": "2023-02-19T14:43+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1676810586312,
      "iso-8601": "2023-02-19T14:43+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/limit",
  "download-rate": 3,
  "download-unit": "gbps",
  "upload-rate": 0,
  "upload-unit": "mbps",
  "enable-download": true,
  "enable-upload": false
}
```
