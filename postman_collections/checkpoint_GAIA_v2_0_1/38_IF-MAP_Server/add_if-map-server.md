# add if-map-server

**Collection:** Web API (version 2.0.1) > 38 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-if-map-server`

## Description

Create new IF-MAP server.

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
  "host": "TestHost",
  "version": 2,
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
  "authentication": {
    "authentication-method": "certificate_based"
  }
}
```

## Example Responses

### Example 1: add if-map-server
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
      "posix": 1746516237691,
      "iso-8601": "2025-05-06T10:23+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746516237691,
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
