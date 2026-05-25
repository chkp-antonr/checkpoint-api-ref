# set lsv-profile

**Collection:** Web API (version 2.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-lsv-profile`

## Description

Edit an existing LSV Profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "existing lsv-profile",
  "certificate-authority": "another CA",
  "restrict-allowed-addresses": "false",
  "vpn-domain.limit-peer-domain-size": "false"
}
```

## Example Responses

### Example 1: set lsv-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0cb15fb6-f1a7-42d5-9eef-64aaef000642",
  "name": "existing lsv-profile",
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
      "posix": 1560440984500,
      "iso-8601": "2019-06-13T18:49+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1560440974324,
      "iso-8601": "2019-06-13T18:49+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Profiles/lsv_profile",
  "certificate-authority": "4f76d696-d7b4-4b89-a1e5-7eea416646c1",
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
  "restrict-allowed-addresses": false,
  "vpn-domain": {
    "limit-peer-domain-size": false,
    "max-allowed-addresses": 256
  }
}
```
