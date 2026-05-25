# add-resource-uri-for-qos

**Collection:** Web API (version 2.0.1) > 44 Resource URI For QOS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-resource-uri-for-qos`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newUriForQosResource",
  "search-for-url": "www.checkpoint.com"
}
```

## Example Responses

### Example 1: add-resource-uri-for-qos
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "82dcf9eb-c2d8-4770-92b9-5b688ab22bec",
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
      "posix": 1745403226820,
      "iso-8601": "2025-04-23T13:13+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1745403226820,
      "iso-8601": "2025-04-23T13:13+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "search-for-url": "www.checkpoint.com"
}
```
