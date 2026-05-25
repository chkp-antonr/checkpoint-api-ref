# add-interoperable-device with external interface

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Adds an Interoperable Device with external interface

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
  "ip-address": "192.168.10.2",
  "interfaces.ip-address": "91.90.143.5",
  "interfaces.network-mask": "255.255.255.0",
  "interfaces.name": "externalInterface",
  "interfaces.topology": "external"
}
```

## Example Responses

### Example 1: add-interoperable-device with external interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0f5cb3be-8a54-4f73-bf81-e0de8f937f26",
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
      "posix": 1633245402916,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633245402916,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.10.2",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": [
    {
      "uid": "94288c6f-d0c0-444f-824d-6b0705073220",
      "name": "externalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "tags": [],
      "comments": "",
      "icon": "Unknown",
      "ipv4-address": "91.90.143.5",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "topology": "external",
      "anti-spoofing": true,
      "anti-spoofing-settings": {
        "action": "prevent",
        "exclude-packets": false,
        "spoof-tracking": "log"
      }
    }
  ]
}
```
