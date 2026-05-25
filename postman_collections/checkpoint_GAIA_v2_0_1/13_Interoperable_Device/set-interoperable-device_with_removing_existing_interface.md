# set-interoperable-device with removing existing interface

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-interoperable-device`

## Description

Sets Interoperable Device with removing existing interface

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
  "interfaces.remove": "externalInterface"
}
```

## Example Responses

### Example 1: set-interoperable-device with removing existing interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "405d329c-cac6-4002-b7ce-b15800c78fcc",
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
      "posix": 1633253999980,
      "iso-8601": "2021-10-03T12:39+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1633250910424,
      "iso-8601": "2021-10-03T11:48+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.10.5",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": []
}
```
