# set-time

**Collection:** Web API (version 2.0.1) > 16 Time
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-time`

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
  "hours-ranges": [
    {
      "from": "00:22",
      "to": "00:33"
    }
  ],
  "recurrence": {
    "pattern": "Weekly",
    "weekdays": [
      "Fri"
    ],
    "month": "Any"
  }
}
```

## Example Responses

### Example 1: set-time
**Status:** `200 OK`
