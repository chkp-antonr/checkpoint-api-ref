# set-time-group

**Collection:** Web API (version 2.1) > 17 Time Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-time-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "timeGroup-1",
  "members": {
    "add": "timeGroup-2"
  }
}
```

## Example Responses

### Example 1: set-time-group
**Status:** `200 OK`
