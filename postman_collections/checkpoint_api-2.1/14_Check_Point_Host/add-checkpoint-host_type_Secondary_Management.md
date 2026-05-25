# add-checkpoint-host type Secondary Management

**Collection:** Web API (version 2.1) > 14 Check Point Host
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-checkpoint-host`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "secondarymgmt",
  "ipv4-address": "5.5.5.5",
  "management-blades": {
    "network-policy-management": true
  }
}
```

## Example Responses

### Example 1: add-checkpoint-host type Secondary Management
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "bd94f71a-13f1-48e7-85ab-9f37484c80d5",
  "name": "secondarymgmt",
  "type": "checkpoint-host",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "5.5.5.5",
  "interfaces": [],
  "version": "R81",
  "os": "Gaia",
  "hardware": "Open server",
  "sic-state": "uninitialized",
  "management-blades": {
    "logging-and-status": false,
    "smart-event-server": false,
    "smart-event-correlation": false,
    "network-policy-management": true,
    "user-directory": false,
    "compliance": false,
    "endpoint-policy": false,
    "secondary": true,
    "identity-logging": false
  },
  "logs-settings": {
    "rotate-log-by-file-size": false,
    "rotate-log-file-size-threshold": 1000,
    "rotate-log-on-schedule": false,
    "alert-when-free-disk-space-below-metrics": "mbytes",
    "alert-when-free-disk-space-below": true,
    "alert-when-free-disk-space-below-threshold": 20,
    "alert-when-free-disk-space-below-type": "popup alert",
    "delete-when-free-disk-space-below-metrics": "mbytes",
    "delete-when-free-disk-space-below": true,
    "delete-when-free-disk-space-below-threshold": 5000,
    "before-delete-keep-logs-from-the-last-days": false,
    "before-delete-keep-logs-from-the-last-days-threshold": 3664,
    "before-delete-run-script": false,
    "before-delete-run-script-command": "",
    "stop-logging-when-free-disk-space-below-metrics": "mbytes",
    "stop-logging-when-free-disk-space-below": false,
    "stop-logging-when-free-disk-space-below-threshold": 100,
    "delete-index-files-older-than-days": false,
    "delete-index-files-older-than-days-threshold": 14,
    "forward-logs-to-log-server": false,
    "update-account-log-every": 3600,
    "detect-new-citrix-ica-application-names": false,
    "turn-on-qos-logging": true,
    "enable-log-indexing": true,
    "smart-event-intro-correlation-unit": true,
    "accept-syslog-messages": false
  },
  "send-alerts-to-server": [
    {
      "uid": "6da0cc30-4ac4-c544-bd20-d8ba9bf7f51c",
      "name": "ice-main-take-183",
      "type": "checkpoint-host",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "send-logs-to-server": [
    {
      "uid": "6da0cc30-4ac4-c544-bd20-d8ba9bf7f51c",
      "name": "ice-main-take-183",
      "type": "checkpoint-host",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "send-logs-to-backup-server": [],
  "save-logs-locally": false
}
```
