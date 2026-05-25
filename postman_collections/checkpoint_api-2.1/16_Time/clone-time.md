# clone-time

**Collection:** Web API (version 2.1) > 16 Time
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-time`

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

### Example 1: clone-time
**Status:** `200 OK`
