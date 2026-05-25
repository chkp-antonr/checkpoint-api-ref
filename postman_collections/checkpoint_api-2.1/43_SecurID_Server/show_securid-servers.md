# show securid-servers

**Collection:** Web API (version 2.1) > 43 SecurID Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-securid-servers`

## Description

Shows SecurID Servers.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5,
  "offset": 0,
  "details-level": "full"
}
```

## Example Responses

### Example 1: show securid-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
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
          "posix": 1746455964429,
          "iso-8601": "2025-05-05T17:39+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746455691244,
          "iso-8601": "2025-05-05T17:34+0300"
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
      "icon": "Objects/account_unit",
      "config-file-name": "NewConfigFile",
      "base64-config-file-content": "Q0xJRU5UX0lQPSAxLjEuMS4yMg=="
    },
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
          "posix": 1746456841671,
          "iso-8601": "2025-05-05T17:54+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746456841671,
          "iso-8601": "2025-05-05T17:54+0300"
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
      "icon": "Objects/account_unit",
      "config-file-name": "NewConfigFile",
      "base64-config-file-content": "Q0xJRU5UX0lQPSAxLjEuMS4yMg=="
    }
  ]
}
```
