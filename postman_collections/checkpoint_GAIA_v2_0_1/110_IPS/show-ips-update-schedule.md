# show-ips-update-schedule

**Collection:** Web API (version 2.0.1) > 110 IPS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-ips-update-schedule`

## Description

Show IPS update schedule

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-ips-update-schedule
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": true,
  "time": "0:00",
  "recurrence": {
    "pattern": "Daily"
  }
}
```
