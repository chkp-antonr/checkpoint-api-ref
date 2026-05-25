# add lsv-profile with restricted encryption domain

**Collection:** Web API (version 2.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/add_lsv_profile_with_restricted_encryption_domain`

## Description

Add an LSV Profile with restricted allowed IP addresses in the VPN Domain

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New lsv-profile",
  "certificate-authority": "dedicated_profile_certificate",
  "restrict-allowed-addresses": "true",
  "allowed-ip-addresses.1": "specific network object"
}
```

## Example Responses

### Example 1: add lsv-profile with restricted encryption domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7e7a98f5-636a-4b96-beac-0f0d54a22ad5",
  "name": "New lsv-profile",
  "type": "lsv-profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1560440635196,
      "iso-8601": "2019-06-13T18:43+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1560440635196,
      "iso-8601": "2019-06-13T18:43+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Profiles/lsv_profile",
  "certificate-authority": "8bd9fce8-75aa-a44f-86e7-a5f95d974562",
  "allowed-ip-addresses": [
    {
      "uid": "2830653f-2e7f-4212-90ef-94fd6378f2d2",
      "name": "supermarket-network",
      "type": "network",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "subnet4": "10.10.0.0",
      "subnet-mask": "255.255.0.0",
      "mask-length4": 16
    }
  ],
  "restrict-allowed-addresses": true,
  "vpn-domain": {
    "limit-peer-domain-size": false,
    "max-allowed-addresses": 256
  }
}
```
