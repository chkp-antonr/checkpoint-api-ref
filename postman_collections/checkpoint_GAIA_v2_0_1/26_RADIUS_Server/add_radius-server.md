# add radius-server

**Collection:** Web API (version 2.0.1) > 26 RADIUS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-radius-server`

## Description

Add radius server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "radServer",
  "server": "hostRad",
  "shared-secret": "123"
}
```

## Example Responses

### Example 1: add radius-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8b7dacd0-fa1d-4d6d-af14-b2a0a1e857d8",
  "name": "radServer",
  "type": "radius-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1656238205387,
      "iso-8601": "2022-06-26T13:10+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1656238205387,
      "iso-8601": "2022-06-26T13:10+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "groups": [],
  "server": {
    "uid": "a9624ccc-5c00-4518-bb2e-1f9065c65e4b",
    "name": "hostrad",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "7.7.7.8"
  },
  "service": {
    "uid": "97aeb41d-9aea-11d5-bd16-0090272ccb30",
    "name": "RADIUS",
    "type": "service-udp",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "Protocols/RADIUS",
    "color": "firebrick",
    "port": "1645"
  },
  "priority": 1,
  "version": "RADIUS Ver. 1.0",
  "protocol": "PAP",
  "accounting": {
    "enable-ip-pool-management": false,
    "accounting-service": {
      "uid": "3af666e6-d36d-491d-9976-26369baaf84b",
      "name": "RADIUS-ACCOUNTING",
      "type": "service-udp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/RADIUS",
      "color": "firebrick",
      "port": "1646"
    }
  }
}
```
