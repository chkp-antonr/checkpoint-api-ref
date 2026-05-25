# set radius-server

**Collection:** Web API (version 2.0.1) > 26 RADIUS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-radius-server`

## Description

Set Radius server name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "t4",
  "server": "hostRadius"
}
```

## Example Responses

### Example 1: set radius-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f99ccf83-dbf9-40b9-9142-cda575b9e956",
  "name": "t4",
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
      "posix": 1656239132247,
      "iso-8601": "2022-06-26T13:25+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1655886006041,
      "iso-8601": "2022-06-22T11:20+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "groups": [
    {
      "uid": "cc17f634-00a9-4b9d-8c0b-2a3c700a3413",
      "name": "myspecialgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "ee5c2c89-d2e9-4b49-a3e5-96ef480be746",
      "name": "radgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "2919ab66-4e95-4025-8492-6ffa6c8f0c38",
      "name": "newgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "51c85bec-4013-48eb-b5f8-ac25b2244002",
      "name": "testgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    }
  ],
  "server": {
    "uid": "fe66b956-726a-49c8-8799-1d7648eef7ed",
    "name": "hostRadius",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "2.1.1.1"
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
      "uid": "706c720f-c90d-4aa4-8ab4-967e3887f2f0",
      "name": "quic",
      "type": "service-udp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Services/UDPService",
      "color": "black",
      "port": "443"
    }
  }
}
```
