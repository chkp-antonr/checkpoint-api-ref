# clone if-map-server

**Collection:** Web API (version 2.1) > 44 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-if-map-server`

## Description

Clone existing IF-MAP server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIfMapServer"
}
```

## Example Responses

### Example 1: clone if-map-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "77f493f1-884d-4a74-9b17-d5753478cc38",
  "name": "TestIfMapServer_Clone",
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
      "posix": 1746516481842,
      "iso-8601": "2025-05-06T10:28+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746516481842,
      "iso-8601": "2025-05-06T10:28+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "version": "2.0",
  "host": {
    "uid": "1e35d71c-c1d8-4f5c-928a-0d9214be10fc",
    "name": "TestHost",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "1.1.1.1"
  },
  "port": 1,
  "path": "path",
  "monitored-ips": [
    {
      "first-ip": "1.1.1.1",
      "last-ip": "1.1.1.2"
    },
    {
      "first-ip": "2.1.1.1",
      "last-ip": "2.1.1.2"
    }
  ],
  "query-whole-ranges": true,
  "authentication": {}
}
```
