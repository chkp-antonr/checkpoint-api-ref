# set-simple-gateway with identity sharing

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1set-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw",
  "identity-awareness": true,
  "identity-awareness-settings": {
    "identity-agent": true,
    "identity-sharing-settings": {
      "share-with-other-gateways": false,
      "receive-from-other-gateways": true,
      "receive-from": "IDServerGW"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with identity sharing
**Status:** `200 OK`
