# show-interoperable-device

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interoperable-device`

## Description

Shows a simple Interoperable Device

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "NewInteroperableDevice"
}
```

## Example Responses

### Example 1: show-interoperable-device
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "294ee992-9651-4665-9594-4c218ce85008",
  "name": "NewInteroperableDevice",
  "type": "interop",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1630482978370,
      "iso-8601": "2021-09-01T10:56+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1630482978370,
      "iso-8601": "2021-09-01T10:56+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.1.6",
  "ipv6-address": "",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": []
}
```
