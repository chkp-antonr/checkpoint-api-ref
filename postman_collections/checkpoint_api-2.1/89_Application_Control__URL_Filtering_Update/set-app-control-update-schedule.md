# set-app-control-update-schedule

**Collection:** Web API (version 2.1) > 89 Application Control & URL Filtering Update
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-app-control-update-schedule`

## Description

Set Application Control & URL Filtering update schedule with interval configuration.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "schedule-gateway-update": {
    "schedule": {
      "recurrence": {
        "pattern": "interval",
        "interval-hours": 4,
        "interval-minutes": 30,
        "interval-seconds": 10
      }
    }
  }
}
```

## Example Responses

### Example 1: set-app-control-update-schedule
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6fe188d4-9db0-4dd6-89ab-4dfe79b3ad46",
  "type": "app-control-update-schedule",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1737982193846,
      "iso-8601": "2025-01-27T14:49+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1736669818197,
      "iso-8601": "2025-01-12T10:16+0200"
    },
    "creator": "System"
  },
  "schedule-management-update": {
    "enabled": true,
    "schedule": {
      "time": "0:00",
      "recurrence": {
        "pattern": "Daily"
      }
    }
  },
  "schedule-gateway-update": {
    "enabled": true,
    "schedule": {
      "time": "1:00",
      "recurrence": {
        "interval-seconds": 10,
        "interval-minutes": 30,
        "interval-hours": 4
      }
    }
  }
}
```
