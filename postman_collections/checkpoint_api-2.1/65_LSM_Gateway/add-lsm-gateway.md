# add-lsm-gateway

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
  }
}
```

## Example Responses

### Example 1: add-lsm-gateway
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f3b6df08-d973-4f16-8cfb-1f9562c6d120",
  "name": "lsm_gateway",
  "type": "lsm-gateway",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1607433843108,
      "iso-8601": "2020-12-08T15:24+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1607433831474,
      "iso-8601": "2020-12-08T15:23+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ROBO/ROBO_CP",
  "security-profile": "lsm_profile",
  "sic-name": "CN=lsm_gateway,O=R81.10_API..wm5cer",
  "sic-state": "Initialized",
  "ip-address": "1.2.3.4",
  "version": "R81.10",
  "os-name": "Gaia",
  "provisioning-state": "using-profile",
  "provisioning-settings": {
    "provisioning-profile": "prv_profile"
  }
}
```
