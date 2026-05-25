# add-time

**Collection:** Web API (version 2.0.1) > 16 Time
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-time`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "timeObject1",
  "start-now": "true",
  "end": {
    "date": "24-Nov-2014",
    "time": "21:22"
  },
  "end-never": "false",
  "hours-ranges": [
    {
      "from": "00:00",
      "to": "00:00",
      "enabled": true,
      "index": 1
    },
    {
      "from": "00:00",
      "to": "00:00",
      "enabled": false,
      "index": 2
    }
  ],
  "recurrence": {
    "pattern": "Daily",
    "month": "Any",
    "weekdays": [
      "Sun",
      "Mon"
    ],
    "days": [
      "1"
    ]
  }
}
```

## Example Responses

### Example 1: add-time
**Status:** `200 OK`
