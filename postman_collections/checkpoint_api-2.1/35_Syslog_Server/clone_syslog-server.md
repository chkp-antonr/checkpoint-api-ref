# clone syslog-server

**Collection:** Web API (version 2.1) > 35 Syslog Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-syslog-server`

## Description

Clones syslog server.

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
  "port": "1000"
}
```

## Example Responses

### Example 1: clone syslog-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "94c872a5-596a-45a3-acc5-865a2cbfaf55",
  "name": "newSyslogServer_Clone",
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
      "posix": 1734428921229,
      "iso-8601": "2024-12-17T11:48+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734428921229,
      "iso-8601": "2024-12-17T11:48+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "port": 1000,
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
