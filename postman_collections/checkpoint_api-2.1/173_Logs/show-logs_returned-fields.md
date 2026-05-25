# show-logs returned-fields

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-logs`

## Description

Selects the columns to be returned, applicable only on regular logs and not grouping.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "new-query": {
    "time-frame": "today",
    "returned-fields": [
      "src",
      "action"
    ],
    "max-logs-per-request": "5"
  }
}
```

## Example Responses

### Example 1: show-logs returned-fields
**Status:** `200 OK`

**Body:**
```javascript
{
  "logs": [
    {
      "src": "13.52.239.27",
      "action": "Drop"
    },
    {
      "src": "91.47.80.66",
      "action": "Accept"
    },
    {
      "src": "208.54.104.100",
      "action": "Accept"
    },
    {
      "src": "192.168.131.199",
      "action": "Accept"
    },
    {
      "src": "85.250.37.204",
      "action": "Drop"
    }
  ],
  "logs-count": 5,
  "query-id": "WEB_API_9c435e4a-a7cf-4e22-8984-411ec495e328"
}
```
