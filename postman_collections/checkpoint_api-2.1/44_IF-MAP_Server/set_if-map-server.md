# set if-map-server

**Collection:** Web API (version 2.1) > 44 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-if-map-server`

## Description

Edit existing IF-MAP server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIfMapServer",
  "host": "TestHost2",
  "port": 2,
  "version": 1.1,
  "path": "newPath",
  "monitored-ips": [
    {
      "first-ip": "3.1.1.1",
      "last-ip": "3.1.1.2"
    }
  ],
  "query-whole-ranges": false
}
```

## Example Responses

### Example 1: set if-map-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8bfafa52-0d11-4a3e-aee7-f9237c92d006",
  "name": "TestIfMapServer",
  "type": "if-map-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1746517085069,
      "iso-8601": "2025-05-06T10:38+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746516237698,
      "iso-8601": "2025-05-06T10:23+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "version": "1.1",
  "host": {
    "uid": "8907f785-4b06-4f0d-82df-d19ea1ecf68a",
    "name": "TestHost2",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "2.2.2.2"
  },
  "port": 2,
  "path": "newPath",
  "monitored-ips": [
    {
      "first-ip": "3.1.1.1",
      "last-ip": "3.1.1.2"
    }
  ],
  "query-whole-ranges": false,
  "authentication": {}
}
```
