# show-hosts

**Collection:** Web API (version 2.0.1) > 05 Host
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-hosts`

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

### Example 1: show-hosts
**Status:** `200 OK`
