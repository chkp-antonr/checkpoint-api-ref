# clone logical server

**Collection:** Web API (version 2.1) > 24 Logical Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-logical-server`

## Description

Clone logical server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "logicalServer1",
  "ip-address": "1.1.1.5",
  "server-group": "new_group"
}
```

## Example Responses

### Example 1: clone logical server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1f40ca0e-ede8-49b8-b1d2-d04168f3ea31",
  "name": "logicalServer1_Clone",
  "type": "logical-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753864136718,
      "iso-8601": "2025-07-30T11:28+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753864136718,
      "iso-8601": "2025-07-30T11:28+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/logical_server",
  "ipv4-address": "1.1.1.5",
  "server-type": "other",
  "server-group": {
    "uid": "ff1b4589-79d7-4e20-80f0-a0e356f4b291",
    "name": "new_group",
    "type": "group",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "General/group",
    "color": "black"
  },
  "persistence-mode": true,
  "balance-method": "random",
  "persistency-type": "by_service"
}
```
