# set-ips-update-schedule-interval

**Collection:** Web API (version 2.0.1) > 110 IPS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-ips-update-schedule`

## Description

Set IPS update schedule (interval basis)

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
  "recurrence": {
    "pattern": "interval",
    "minutes": 145
  }
}
```

## Example Responses

### Example 1: set-ips-update-schedule-interval
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": true,
  "recurrence": {
    "pattern": "Interval",
    "minutes": 45
  }
}
```
