# set-interoperable-device

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-interoperable-device`

## Description

Sets simple Interoperable Device

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
  "ip-address": "192.168.1.6"
}
```

## Example Responses

### Example 1: set-interoperable-device
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3b330a2b-d626-49c6-864a-2309a6d2957e",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.1.6",
  "interfaces": [],
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw",
    "vpn-domain-exclude-external-ip-addresses": false
  },
  "groups": [],
  "tags": [],
  "autonomous-system-number": "0",
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734275506774,
      "iso-8601": "2024-12-15T17:11+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734275245188,
      "iso-8601": "2024-12-15T17:07+0200"
    },
    "creator": "aa"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
