# show-administrators

**Collection:** Web API (version 2.1) > 155 Administrator
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-administrators`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-administrators
**Status:** `200 OK`
