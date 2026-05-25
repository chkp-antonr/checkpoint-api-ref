# set-lsm-gateway

**Collection:** Web API (version 2.0.1) > 58 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-lsm-gateway`

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
  }
}
```

## Example Responses

### Example 1: set-lsm-gateway
**Status:** `200 OK`
