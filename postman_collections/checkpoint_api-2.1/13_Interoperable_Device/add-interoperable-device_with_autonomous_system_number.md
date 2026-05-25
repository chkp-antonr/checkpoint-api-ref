# add-interoperable-device with autonomous system number

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interoperable-device`

## Description

Adds an Interoperable Device with custom Autonomous System Number

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "NewInteroperableDevice",
  "ip-address": "172.15.5.5",
  "asn": 65522
}
```

## Example Responses

### Example 1: add-interoperable-device with autonomous system number
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d1410884-164b-4ccf-b8f5-eaafbc77561e",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "172.15.5.5",
  "interfaces": [],
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw",
    "vpn-domain-exclude-external-ip-addresses": false
  },
  "groups": [],
  "tags": [],
  "autonomous-system-number": "65522",
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734300473137,
      "iso-8601": "2024-12-16T00:07+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734300473137,
      "iso-8601": "2024-12-16T00:07+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
