# set-simple-gateway with advanced settings

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-gateway`

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
  "advanced-settings": {
    "connection-persistence": "keep-all-connections",
    "sam": {
      "forward-to-other-sam-servers": true,
      "use-early-versions": {
        "enabled": "true",
        "compatibility-mode": "ssl_clear_opsec"
      },
      "purge-sam-file": {
        "enabled": "true",
        "purge-when-size-reaches-to": "150"
      }
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with advanced settings
**Status:** `200 OK`
