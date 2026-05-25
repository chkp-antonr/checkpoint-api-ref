# set-simple-gateway with hit count

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
  "hit-count": true
}
```

## Example Responses

### Example 1: set-simple-gateway with hit count
**Status:** `200 OK`
