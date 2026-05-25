# set-automatic-purge by last period

**Collection:** Web API (version 2.1) > 04 Automatic Purge
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-automatic-purge`

## Description

Schedule Automatic Purge to all sessions except the newest sessions from last days (last 30 days) to preserve. The purge action will be executed every 5 days started from 2020-04-18 at 18:00:00

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "enabled": true,
  "keep-sessions-by-count": false,
  "number-of-days-to-keep": "30",
  "scheduling.check-interval": "5",
  "scheduling.time-units": "days",
  "scheduling.start-date": "2020-04-18T18:00:00"
}
```

## Example Responses

### Example 1: set-automatic-purge by last period
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": true,
  "keep-sessions-by-count": false,
  "number-of-sessions-to-keep": "0",
  "keep-sessions-by-days": true,
  "number-of-days-to-keep": "30",
  "scheduling": {
    "check-interval": 5,
    "time-units": "days",
    "start-date": "2020-04-18T18:00:00",
    "last-check": "",
    "next-check": "2020-04-18T18:00:00"
  }
}
```
