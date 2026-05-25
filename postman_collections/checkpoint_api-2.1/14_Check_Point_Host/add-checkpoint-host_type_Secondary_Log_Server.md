# add-checkpoint-host type Secondary Log Server

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
  "name": "secondarylogserver",
  "ipv4-address": "5.5.5.5",
  "management-blades": {
    "network-policy-management": true,
    "logging-and-status": true
  }
}
```

## Example Responses

### Example 1: add-checkpoint-host type Secondary Log Server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f50f3810-d16c-4239-88d0-9f37ac581387",
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
    "logging-and-status": true,
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
  }
}
```
