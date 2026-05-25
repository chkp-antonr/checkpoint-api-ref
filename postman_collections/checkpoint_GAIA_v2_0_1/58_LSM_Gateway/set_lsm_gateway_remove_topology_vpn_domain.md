# set lsm gateway remove topology vpn domain

**Collection:** Web API (version 2.0.1) > 58 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-lsm-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "lsm_gateway",
  "topology": {
    "manual-vpn-domain": {
      "remove": {
        "from-ipv4-address": "10.10.10.1",
        "to-ipv4-address": "10.10.10.2",
        "comments": "range 1"
      }
    }
  }
}
```

## Example Responses

### Example 1: set lsm gateway remove topology vpn domain
**Status:** `200 OK`
