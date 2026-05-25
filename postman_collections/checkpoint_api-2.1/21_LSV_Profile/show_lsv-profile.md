# show lsv-profile

**Collection:** Web API (version 2.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-lsv-profile`

## Description

Show information of an LSV Profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "existing lsv-profile"
}
```

## Example Responses

### Example 1: show lsv-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "160de00a-c8b8-4cb4-ae4b-8623d0e6f8b6",
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
      "posix": 1562087584480,
      "iso-8601": "2019-07-02T20:13+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1562087584480,
      "iso-8601": "2019-07-02T20:13+0300"
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
    "limit-peer-domain-size": false,
    "max-allowed-addresses": 256
  },
  "allowed-ip-addresses": [],
  "restrict-allowed-addresses": false
}
```
