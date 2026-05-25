# set-simple-cluster with identity sharing

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

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
  "ip-address": "1.2.3.4",
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

### Example 1: set-simple-cluster with identity sharing
**Status:** `200 OK`
