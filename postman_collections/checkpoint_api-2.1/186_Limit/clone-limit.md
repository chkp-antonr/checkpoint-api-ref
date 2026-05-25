# clone-limit

**Collection:** Web API (version 2.1) > 186 Limit
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-limit`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "limit_obj"
}
```

## Example Responses

### Example 1: clone-limit
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "85d46c45-5c87-4d7a-a686-84d1be3d1482",
  "name": "limit_obj_Clone",
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
      "posix": 1676811256388,
      "iso-8601": "2023-02-19T14:54+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1676811256388,
      "iso-8601": "2023-02-19T14:54+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/limit",
  "download-rate": 50,
  "download-unit": "kbps",
  "upload-rate": 0,
  "upload-unit": "mbps",
  "enable-download": true,
  "enable-upload": false
}
```
