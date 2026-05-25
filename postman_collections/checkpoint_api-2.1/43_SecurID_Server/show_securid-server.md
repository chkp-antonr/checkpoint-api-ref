# show securid-server

**Collection:** Web API (version 2.1) > 43 SecurID Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-securid-server`

## Description

Shows SecurID server.

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

### Example 1: show securid-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "62d8fbbd-b36b-4b53-88f2-fa28a314b6b4",
  "name": "TestSecurIdServer",
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
      "posix": 1746455964412,
      "iso-8601": "2025-05-05T17:39+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746455691244,
      "iso-8601": "2025-05-05T17:34+0300"
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
