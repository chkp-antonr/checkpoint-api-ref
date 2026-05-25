# set-ha-state

**Collection:** Web API (version 2.0.1) > 143 High Availability
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-ha-state`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "new-state": "active"
}
```

## Example Responses

### Example 1: set-ha-state
**Status:** `200 OK`
