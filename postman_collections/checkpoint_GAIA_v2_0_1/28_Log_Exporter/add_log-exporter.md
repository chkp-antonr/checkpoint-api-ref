# add log-exporter

**Collection:** Web API (version 2.0.1) > 28 Log Exporter
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-log-exporter`

## Description

Create new log exporter.

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
  "target-server": "1.2.3.4",
  "target-port": 1234,
  "protocol": "tcp",
  "attachments": {
    "add-link-to-log-attachment": true
  }
}
```

## Example Responses

### Example 1: add log-exporter
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "824eed1a-e010-4f7f-a9c2-8d5c82119340",
  "name": "newLogExporter",
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
      "posix": 1734427947740,
      "iso-8601": "2024-12-17T11:32+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734427947740,
      "iso-8601": "2024-12-17T11:32+0200"
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
  "target-port": 1234,
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
