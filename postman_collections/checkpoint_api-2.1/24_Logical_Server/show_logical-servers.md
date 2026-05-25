# show logical-servers

**Collection:** Web API (version 2.1) > 24 Logical Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-logical-servers`

## Description

Retrieve all logical servers.

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

### Example 1: show logical-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "165ea393-fd9a-4af7-9c52-e8e5816af890",
      "name": "logicalServer2",
      "type": "logical-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "locked by current session",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1753281830332,
          "iso-8601": "2025-07-23T17:43+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1753281830332,
          "iso-8601": "2025-07-23T17:43+0300"
        },
        "creator": "aa"
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
      "icon": "Objects/logical_server",
      "ipv4": "3.4.5.6",
      "server-type": "http",
      "server-group": {
        "uid": "a2583ccb-d3b0-49ea-8b7a-64e1ad8a8ffb",
        "name": "testGroup",
        "type": "group",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "meta-info": {
          "lock": "locked by current session",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1753177459070,
            "iso-8601": "2025-07-22T12:44+0300"
          },
          "last-modifier": "aa",
          "creation-time": {
            "posix": 1753177459070,
            "iso-8601": "2025-07-22T12:44+0300"
          },
          "creator": "aa"
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
        "icon": "General/group",
        "groups": [],
        "members": []
      },
      "persistence-mode": true,
      "balance-method": "domain",
      "persistency-type": "by_server"
    }
  ]
}
```
