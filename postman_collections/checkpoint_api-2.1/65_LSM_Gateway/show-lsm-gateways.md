# show-lsm-gateways

**Collection:** Web API (version 2.1) > 65 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-lsm-gateways`

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

### Example 1: show-lsm-gateways
**Status:** `200 OK`
