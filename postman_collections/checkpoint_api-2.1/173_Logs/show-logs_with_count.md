# show-logs with count

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-logs`

## Description

Query the number of total logs. Can be used with filters to find logs count for specific search.

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
    "show-total-record-count": true
  }
}
```

## Example Responses

### Example 1: show-logs with count
**Status:** `200 OK`

**Body:**
```javascript
{
  "logs-count": 321146
}
```
