# add-interoperable-device with IPv4 address

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Adds Interoperable Device with IPv4 address

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
  "ipv4-address": "192.168.1.6"
}
```

## Example Responses

### Example 1: add-interoperable-device with IPv4 address
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "52739378-16f2-4b9a-ad16-53c99bba964f",
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
      "posix": 1630476929652,
      "iso-8601": "2021-09-01T09:15+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1630476929652,
      "iso-8601": "2021-09-01T09:15+0300"
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
  "ipv6-address": "",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": []
}
```
