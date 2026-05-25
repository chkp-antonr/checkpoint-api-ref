# clone log-exporter

**Collection:** Web API (version 2.0.1) > 28 Log Exporter
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-log-exporter`

## Description

Clone existing log exporter.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newLogExporter",
  "target-port": "9306"
}
```

## Example Responses

### Example 1: clone log-exporter
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b39f64ff-cb5f-4aa0-ad1f-a0e861350b94",
  "name": "newLogExporter_Clone",
  "type": "log-exporter",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734428079834,
      "iso-8601": "2024-12-17T11:34+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734428079834,
      "iso-8601": "2024-12-17T11:34+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/log_exporter",
  "target-server": "1.2.3.4",
  "target-port": 9306,
  "protocol": "tcp",
  "enabled": true,
  "attachments": {
    "add-link-to-log-details": false,
    "add-link-to-log-attachment": true,
    "add-log-attachment-id": false
  },
  "data-manipulation": {
    "format": "syslog",
    "aggregate-log-updates": "true"
  }
}
```
