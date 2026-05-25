# set-simple-cluster with advanced settings

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
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

### Example 1: set-simple-cluster with advanced settings
**Status:** `200 OK`
