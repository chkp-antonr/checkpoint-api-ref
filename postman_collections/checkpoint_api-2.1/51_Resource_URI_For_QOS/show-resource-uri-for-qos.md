# show-resource-uri-for-qos

**Collection:** Web API (version 2.1) > 51 Resource URI For QOS
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-resource-uri-for-qos`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newUriForQosResource"
}
```

## Example Responses

### Example 1: show-resource-uri-for-qos
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2119f209-4151-4093-bdec-603c180cc046",
  "name": "my-url",
  "type": "resource-uri-for-qos",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1745412248609,
      "iso-8601": "2025-04-23T15:44+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1745412045949,
      "iso-8601": "2025-04-23T15:40+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "search-for-url": "www.checkpoint.com"
}
```
