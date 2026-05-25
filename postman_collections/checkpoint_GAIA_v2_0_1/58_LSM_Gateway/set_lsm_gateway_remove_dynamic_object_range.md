# set lsm gateway remove dynamic object range

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
  "dynamic-objects": {
    "set": {
      "name": "dynamic_object_name",
      "resolved-ip-addresses": {
        "remove": {
          "ipv4-address": "10.10.10.1"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: set lsm gateway remove dynamic object range
**Status:** `200 OK`
