# add logical server

**Collection:** Web API (version 2.1) > 24 Logical Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-logical-server`

## Description

Add new logical server

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
  "ip-address": "1.1.1.1",
  "server-group": "testGroup",
  "server-type": "other",
  "persistence-mode": true,
  "persistency-type": "by_server",
  "balance-method": "domain"
}
```

## Example Responses

### Example 1: add logical server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c1ad5eda-b496-4e2c-b1c4-343292f707e4",
  "name": "logicalServer1",
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
      "posix": 1753280308534,
      "iso-8601": "2025-07-23T17:18+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753280308534,
      "iso-8601": "2025-07-23T17:18+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/logical_server",
  "ipv4": "1.1.1.1",
  "server-type": "other",
  "server-group": {
    "uid": "a2583ccb-d3b0-49ea-8b7a-64e1ad8a8ffb",
    "name": "testGroup",
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
  "balance-method": "domain",
  "persistency-type": "by_server"
}
```
