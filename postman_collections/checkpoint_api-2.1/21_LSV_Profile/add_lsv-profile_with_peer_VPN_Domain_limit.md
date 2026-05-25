# add lsv-profile with peer VPN Domain limit

**Collection:** Web API (version 2.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/add_lsv_profile_with_peer_VPN_Domain_limit`

## Description

Add an LSV Profile with a maximum number of IP addresses in the VPN Domain of each peer

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
  "vpn-domain.limit-peer-domain-size": "true",
  "vpn-domain.max-allowed-addresses": "128"
}
```

## Example Responses

### Example 1: add lsv-profile with peer VPN Domain limit
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2a92e113-f95d-4484-9acf-274edcc0eb5e",
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
      "posix": 1562087992667,
      "iso-8601": "2019-07-02T20:19+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1562087992667,
      "iso-8601": "2019-07-02T20:19+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Profiles/lsv_profile",
  "certificate-authority": "896977ae-64d3-e44f-945d-148def7383f7",
  "vpn-domain": {
    "limit-peer-domain-size": true,
    "max-allowed-addresses": 128
  },
  "allowed-ip-addresses": [],
  "restrict-allowed-addresses": false
}
```
