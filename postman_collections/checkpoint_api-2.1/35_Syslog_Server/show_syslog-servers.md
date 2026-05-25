# show syslog-servers

**Collection:** Web API (version 2.1) > 35 Syslog Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-syslog-servers`

## Description

Shows syslog servers.

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

### Example 1: show syslog-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
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
          "posix": 1734428817643,
          "iso-8601": "2024-12-17T11:46+0200"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1734428817643,
          "iso-8601": "2024-12-17T11:46+0200"
        },
        "creator": "WEB_API"
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
      "icon": "Objects/account_unit",
      "port": 18889,
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1734428812048,
            "iso-8601": "2024-12-17T11:46+0200"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1734428812048,
            "iso-8601": "2024-12-17T11:46+0200"
          },
          "creator": "WEB_API"
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
        "icon": "Objects/host",
        "groups": [],
        "nat-settings": {
          "auto-rule": false
        },
        "ipv4-address": "1.1.1.1",
        "interfaces": []
      }
    },
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
          "posix": 1734428921253,
          "iso-8601": "2024-12-17T11:48+0200"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1734428921253,
          "iso-8601": "2024-12-17T11:48+0200"
        },
        "creator": "WEB_API"
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1734428812048,
            "iso-8601": "2024-12-17T11:46+0200"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1734428812048,
            "iso-8601": "2024-12-17T11:46+0200"
          },
          "creator": "WEB_API"
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
        "icon": "Objects/host",
        "groups": [],
        "nat-settings": {
          "auto-rule": false
        },
        "ipv4-address": "1.1.1.1",
        "interfaces": []
      }
    }
  ]
}
```
