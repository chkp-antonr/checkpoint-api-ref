# set-checkpoint-host

**Collection:** Web API (version 2.0.1) > 14 Check Point Host
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-checkpoint-host`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "secondarylogserver",
  "hardware": "Smart-1",
  "os": "Linux",
  "management-blades": {
    "network-policy-management": true,
    "compliance": true,
    "user-directory": true
  }
}
```

## Example Responses

### Example 1: set-checkpoint-host
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "9e1eba23-6341-4b65-8341-1a5c6c95f4df",
  "name": "secondarylogserver",
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
  "icon": "NetworkObjects/CheckPoint/Hosts/xHost_CP",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "5.5.5.5",
  "interfaces": [],
  "version": "R81",
  "os": "Linux",
  "hardware": "Smart-1",
  "sic-state": "uninitialized",
  "management-blades": {
    "logging-and-status": true,
    "smart-event-server": false,
    "smart-event-correlation": false,
    "network-policy-management": true,
    "user-directory": true,
    "compliance": true,
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
  }
}
```
