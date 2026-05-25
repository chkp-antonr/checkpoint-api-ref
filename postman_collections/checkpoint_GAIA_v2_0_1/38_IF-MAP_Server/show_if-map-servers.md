# show if-map-servers

**Collection:** Web API (version 2.0.1) > 38 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-if-map-servers`

## Description

Shows all IF-MAP servers.

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

### Example 1: show if-map-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "objects": [
    {
      "uid": "7ac821ea-ee1b-4bbd-a45a-ec9e7782876e",
      "name": "TestIfMap",
      "type": "if-map-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "locked by other session",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1746427298675,
          "iso-8601": "2025-05-05T09:41+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1746420979851,
          "iso-8601": "2025-05-05T07:56+0300"
        },
        "creator": "aa",
        "locking-admin": "aa",
        "locking-session-id": "c1dbc2b5-dc9b-4628-b52b-4de66a59fde8"
      },
      "available-actions": {
        "edit": "false",
        "delete": "false",
        "clone": "true"
      },
      "tags": [],
      "read-only": true,
      "comments": "",
      "color": "black",
      "icon": "Objects/account_unit",
      "version": "2.0",
      "host": {
        "uid": "4a2f8b82-4ac0-0644-91ca-ad8bfd2a67e8",
        "name": "mgmt_172.23.48.145mgmt_vs_8210_take_83MGMTdorbe",
        "type": "checkpoint-host",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "meta-info": {
          "lock": "locked by other session",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1746451707203,
            "iso-8601": "2025-05-05T16:28+0300"
          },
          "last-modifier": "aa",
          "creation-time": {
            "posix": 1743103852340,
            "iso-8601": "2025-03-27T21:30+0200"
          },
          "creator": "System",
          "locking-admin": "aa",
          "locking-session-id": "795b39da-7246-4832-8ee1-6a8332da840f"
        },
        "available-actions": {
          "edit": "true",
          "delete": "false",
          "clone": "not_supported"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "NetworkObjects/management",
        "groups": [],
        "nat-settings": {
          "enable-address-translation": false
        },
        "ipv4-address": "172.23.48.145",
        "interfaces": [
          {
            "uid": "a0d11d97-3602-43d3-bb52-a96dcee74753",
            "name": "eth0",
            "type": "CpmiInterface",
            "domain": {
              "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
              "name": "SMC User",
              "domain-type": "domain"
            },
            "tags": [],
            "comments": "",
            "color": "black",
            "icon": "Unknown",
            "subnet4": "172.23.48.145",
            "subnet-mask": "255.255.252.0",
            "mask-length4": 22
          }
        ],
        "version": "R82.10",
        "os": "Gaia",
        "hardware": "Open server",
        "sic-name": "cn=cp_mgmt,o=172.23.48.145mgmt_vs_8210_take_83MGMTdorbe.checkpoint.com.wt2usw",
        "sic-state": "communicating",
        "management-blades": {
          "logging-and-status": true,
          "smart-event-server": false,
          "smart-event-correlation": false,
          "network-policy-management": true,
          "user-directory": false,
          "compliance": true,
          "endpoint-policy": false,
          "secondary": false,
          "identity-logging": false
        },
        "logs-settings": {
          "rotate-log-by-file-size": false,
          "rotate-log-file-size-threshold": 1000,
          "rotate-log-on-schedule": false,
          "alert-when-free-disk-space-below-metrics": "mbytes",
          "alert-when-free-disk-space-below": true,
          "alert-when-free-disk-space-below-threshold": 3000,
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
          "smart-event-intro-correlation-unit": false,
          "accept-syslog-messages": false,
          "distribute-logs-between-all-active-servers": false
        },
        "firewall": false
      },
      "port": 1,
      "path": "path",
      "monitored-ips": [
        {
          "first-ip": "1.0.0.0",
          "last-ip": "1.1.0.0"
        }
      ],
      "query-whole-ranges": true,
      "authentication": {}
    },
    {
      "uid": "8bfafa52-0d11-4a3e-aee7-f9237c92d006",
      "name": "TestIfMapServer",
      "type": "if-map-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1746517085082,
          "iso-8601": "2025-05-06T10:38+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746516237698,
          "iso-8601": "2025-05-06T10:23+0300"
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
      "version": "1.1",
      "host": {
        "uid": "8907f785-4b06-4f0d-82df-d19ea1ecf68a",
        "name": "TestHost2",
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
            "posix": 1746517081334,
            "iso-8601": "2025-05-06T10:38+0300"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1746517081334,
            "iso-8601": "2025-05-06T10:38+0300"
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
        "ipv4-address": "2.2.2.2",
        "interfaces": []
      },
      "port": 2,
      "path": "newPath",
      "monitored-ips": [
        {
          "first-ip": "3.1.1.1",
          "last-ip": "3.1.1.2"
        }
      ],
      "query-whole-ranges": false,
      "authentication": {}
    },
    {
      "uid": "77f493f1-884d-4a74-9b17-d5753478cc38",
      "name": "TestIfMapServer_Clone",
      "type": "if-map-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1746516481888,
          "iso-8601": "2025-05-06T10:28+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746516481888,
          "iso-8601": "2025-05-06T10:28+0300"
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
      "version": "2.0",
      "host": {
        "uid": "1e35d71c-c1d8-4f5c-928a-0d9214be10fc",
        "name": "TestHost",
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
            "posix": 1746516171385,
            "iso-8601": "2025-05-06T10:22+0300"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1746516171385,
            "iso-8601": "2025-05-06T10:22+0300"
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
      },
      "port": 1,
      "path": "path",
      "monitored-ips": [
        {
          "first-ip": "1.1.1.1",
          "last-ip": "1.1.1.2"
        },
        {
          "first-ip": "2.1.1.1",
          "last-ip": "2.1.1.2"
        }
      ],
      "query-whole-ranges": true,
      "authentication": {}
    }
  ]
}
```
