# set-automatic-purge by count

**Collection:** Web API (version 2.0.1) > 04 Automatic Purge
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-automatic-purge`

## Description

Schedule Automatic Purge to all sessions except the specified 10 newest sessions to preserve. The purge action will be executed every 3 weeks started from 2020-04-24 at 12:00:00

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
  "keep-sessions-by-days": false,
  "number-of-sessions-to-keep": "10",
  "scheduling.check-interval": "21",
  "scheduling.time-units": "days",
  "scheduling.start-date": "2020-04-24T12:00:00"
}
```

## Example Responses

### Example 1: set-automatic-purge by count
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": true,
  "keep-sessions-by-count": true,
  "number-of-sessions-to-keep": "10",
  "keep-sessions-by-days": false,
  "number-of-days-to-keep": "0",
  "scheduling": {
    "check-interval": 21,
    "time-units": "days",
    "start-date": "2020-04-24T12:00:00",
    "last-check": "",
    "next-check": "2020-04-24T12:00:00"
  }
}
```
