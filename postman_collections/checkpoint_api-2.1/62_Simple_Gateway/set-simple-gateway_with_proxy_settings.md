# set-simple-gateway with proxy settings

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
  "name": "test_gateway",
  "proxy-settings": {
    "use-custom-proxy": true,
    "proxy-server": "checkpoint",
    "port": "8080"
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with proxy settings
**Status:** `200 OK`
