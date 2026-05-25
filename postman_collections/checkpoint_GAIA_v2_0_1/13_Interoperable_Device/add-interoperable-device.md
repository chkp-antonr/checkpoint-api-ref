# add-interoperable-device

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Adds simple Interoperable Device

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

### Example 1: add-interoperable-device
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "039ab8fa-c6f1-4d57-8395-da2e45674abf",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1632994540158,
      "iso-8601": "2021-09-30T12:35+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1632994540158,
      "iso-8601": "2021-09-30T12:35+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.1.6",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": []
}
```
