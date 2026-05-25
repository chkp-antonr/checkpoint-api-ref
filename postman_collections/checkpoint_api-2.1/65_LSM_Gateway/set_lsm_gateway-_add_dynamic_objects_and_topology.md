# set lsm gateway- add dynamic objects and topology

**Collection:** Web API (version 2.1) > 65 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-lsm-gateway`

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
  "dynamic-objects": {
    "add": {
      "name": "dynamic-object-name",
      "resolved-ip-addresses": {
        "add": {
          "ipv4-address": "10.10.10.1"
        }
      }
    }
  },
  "topology": {
    "vpn-domain": "manual",
    "manual-vpn-domain": {
      "add": {
        "from-ipv4-address": "10.10.10.1",
        "to-ipv4-address": "10.10.10.2",
        "comments": "range 1"
      }
    }
  }
}
```

## Example Responses

### Example 1: set lsm gateway- add dynamic objects and topology
**Status:** `200 OK`
