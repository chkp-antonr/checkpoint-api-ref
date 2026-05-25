# show-interoperable-device with interface

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interoperable-device`

## Description

Shows an Interoperable Device with interface

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

### Example 1: show-interoperable-device with interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7aa983df-10fa-44bf-a871-6ed9388c808a",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1633245403181,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633245403181,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.10.4",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": [
    {
      "uid": "4f2fe133-6745-4c91-82ba-0d4a2938640e",
      "name": "externalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "tags": [],
      "comments": "",
      "color": "black",
      "icon": "Unknown",
      "ipv4-address": "91.90.143.5",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "topology": "external",
      "anti-spoofing": true,
      "anti-spoofing-settings": {
        "action": "detect",
        "exclude-packets": false,
        "spoof-tracking": "alert"
      }
    }
  ]
}
```
