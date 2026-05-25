# show-logs group function with sort

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-logs`

## Description

Sorts the groups by count (default) or a given field, in a descending/ascending order.

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
      ],
      "returned-fields": [
        {
          "fields": [
            "file_size"
          ],
          "function": "max"
        }
      ]
    },
    "sort": [
      {
        "field": "file_size",
        "order": "descending"
      }
    ]
  }
}
```

## Example Responses

### Example 1: show-logs group function with sort
**Status:** `200 OK`

**Body:**
```javascript
{
  "statistics": [
    {
      "src": "192.168.142.82",
      "count": "2",
      "file_size": "5161519"
    },
    {
      "src": "172.20.83.150",
      "count": "1",
      "file_size": "447540"
    },
    {
      "src": "118.76.11.108",
      "count": "2",
      "file_size": "301260"
    },
    {
      "src": "172.20.83.59",
      "count": "1",
      "file_size": "253115"
    },
    {
      "src": "171.76.23.12",
      "count": "1",
      "file_size": "107115"
    }
  ],
  "response-group-limit": 5,
  "reach-group-limit": false
}
```
