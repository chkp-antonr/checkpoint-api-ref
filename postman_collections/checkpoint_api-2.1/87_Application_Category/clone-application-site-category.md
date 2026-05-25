# clone-application-site-category

**Collection:** Web API (version 2.1) > 87 Application Category
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-application-site-category`

## Description

Clone existing application site category

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Category 1"
}
```

## Example Responses

### Example 1: clone-application-site-category
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4617bb40-6168-4685-a901-e7385bc3d57e",
  "name": "New Application Site Category 1_Clone",
  "type": "application-site-category",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747514503347,
      "iso-8601": "2025-05-17T23:41+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1747514503347,
      "iso-8601": "2025-05-17T23:41+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/category",
  "groups": [],
  "description": "My Application Site category",
  "user-defined": true
}
```
