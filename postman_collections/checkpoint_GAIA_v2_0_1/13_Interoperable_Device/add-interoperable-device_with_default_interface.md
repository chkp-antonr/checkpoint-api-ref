# add-interoperable-device with default interface

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Adds an Interoperable Device with default interface

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
  "ip-address": "192.168.10.1",
  "interfaces.ip-address": "100.150.200.0",
  "interfaces.network-mask": "255.255.255.0",
  "interfaces.name": "internalInterface"
}
```

## Example Responses

### Example 1: add-interoperable-device with default interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "fa094741-761e-4c44-931e-e31cd80e6dca",
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
      "posix": 1633250945244,
      "iso-8601": "2021-10-03T11:49+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633250945244,
      "iso-8601": "2021-10-03T11:49+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.10.1",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": [
    {
      "uid": "93d247f5-8c63-46b7-a863-5bc6e3218eba",
      "name": "internalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "tags": [],
      "comments": "",
      "icon": "Unknown",
      "ipv4-address": "100.150.200.0",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "topology": "internal",
      "topology-settings": {
        "ip-address-behind-this-interface": "not defined",
        "interface-leads-to-dmz": false
      },
      "anti-spoofing": false
    }
  ]
}
```
