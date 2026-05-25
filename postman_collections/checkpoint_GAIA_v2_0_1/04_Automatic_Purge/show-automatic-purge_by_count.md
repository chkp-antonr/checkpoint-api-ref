# show-automatic-purge by count

**Collection:** Web API (version 2.0.1) > 04 Automatic Purge
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-automatic-purge`

## Description

Show scheduled Automatic Purge parameters

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

### Example 1: show-automatic-purge by count
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": true,
  "keep-sessions-by-count": true,
  "number-of-sessions-to-keep": "10",
  "keep-sessions-by-days": true,
  "number-of-days-to-keep": "365",
  "scheduling": {
    "check-interval": 21,
    "time-units": "days",
    "start-date": "2020-04-24T12:00:00",
    "last-check": "2020-04-24T12:00:00",
    "next-check": "2020-05-15T12:00:00"
  }
}
```
