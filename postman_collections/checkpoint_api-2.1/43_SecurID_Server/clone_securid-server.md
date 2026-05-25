# clone securid-server

**Collection:** Web API (version 2.1) > 43 SecurID Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-securid-server`

## Description

Clones SecurID server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSecurIdServer"
}
```

## Example Responses

### Example 1: clone securid-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b69a945c-b4ed-4eb0-9c3b-a4348a1d60ba",
  "name": "TestSecurIdServer_Clone",
  "type": "securid-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1746456841664,
      "iso-8601": "2025-05-05T17:54+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746456841664,
      "iso-8601": "2025-05-05T17:54+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "config-file-name": "NewConfigFile",
  "base64-config-file-content": "Q0xJRU5UX0lQPSAxLjEuMS4yMg=="
}
```
