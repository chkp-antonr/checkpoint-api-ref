# add lsm gateway with dynamic objects and topology

**Collection:** Web API (version 2.1) > 65 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-lsm-gateway`

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
  "security-profile": "lsm_profile",
  "sic": {
    "ip-address": "1.2.3.4",
    "one-time-password": "aaaa"
  },
  "provisioning-state": "using-profile",
  "provisioning-settings": {
    "provisioning-profile": "prv_profile"
  },
  "device-id": "id_1",
  "dynamic-objects": [
    {
      "name": "dynamic_object_1",
      "resolved-ip-addresses": [
        {
          "ipv4-address": "3.3.3.3"
        },
        {
          "ipv4-address-range": {
            "from-ipv4-address": "1.1.1.1",
            "to-ipv4-address": "2.2.2.2"
          }
        }
      ]
    },
    {
      "name": "dynamic_object_2",
      "resolved-ip-addresses": [
        {
          "ipv4-address": "4.4.4.4"
        },
        {
          "ipv4-address-range": {
            "from-ipv4-address": "5.5.5.5",
            "to-ipv4-address": "6.6.6.6"
          }
        }
      ]
    }
  ],
  "topology": {
    "vpn-domain": "manual",
    "manual-vpn-domain": [
      {
        "from-ipv4-address": "10.10.10.1",
        "to-ipv4-address": "10.10.10.2",
        "comments": "range 1"
      },
      {
        "from-ipv4-address": "20.20.20.1",
        "to-ipv4-address": "20.20.20.2",
        "comments": "range 2"
      }
    ]
  }
}
```

## Example Responses

### Example 1: add lsm gateway with dynamic objects and topology
**Status:** `200 OK`
