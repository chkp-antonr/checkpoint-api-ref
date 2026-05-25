# set syslog-server

**Collection:** Web API (version 2.0.1) > 29 Syslog Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-syslog-server`

## Description

Edits port of syslog server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newSyslogServer",
  "port": "10101"
}
```

## Example Responses

### Example 1: set syslog-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "9e33fe65-98cd-45f9-baa6-ef06a3484111",
  "name": "newSyslogServer",
  "type": "syslog-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734429173765,
      "iso-8601": "2024-12-17T11:52+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734428817643,
      "iso-8601": "2024-12-17T11:46+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "port": 10101,
  "version": "syslog",
  "host": {
    "uid": "559891be-1b9e-42bf-9acb-f05fadb45313",
    "name": "syslogServerHost",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "1.1.1.1"
  }
}
```
