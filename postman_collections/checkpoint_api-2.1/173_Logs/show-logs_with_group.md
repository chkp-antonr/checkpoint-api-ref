# show-logs with group

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-logs`

## Description

Group logs based on the selected fields.

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
    "group": {
      "by": [
        "src"
      ]
    }
  }
}
```

## Example Responses

### Example 1: show-logs with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "statistics": [
    {
      "src": "194.29.34.164",
      "count": "6974"
    },
    {
      "src": "54.236.233.159",
      "count": "6713"
    },
    {
      "src": "54.236.226.9",
      "count": "6533"
    },
    {
      "src": "52.55.254.133",
      "count": "6374"
    },
    {
      "src": "194.29.38.64",
      "count": "3891"
    }
  ],
  "response-group-limit": 5,
  "reach-group-limit": false
}
```
