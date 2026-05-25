# set-interoperable-device with a new set of interface

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-interoperable-device`

## Description

Sets Interoperable Device with a new set of interface

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
  "interfaces.ip-address": "192.168.10.8",
  "interfaces.mask-length": "24",
  "interfaces.name": "internalInterface"
}
```

## Example Responses

### Example 1: set-interoperable-device with a new set of interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4a51636d-e4e3-44d8-9ef8-f592b2f387f7",
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
      "posix": 1633250949621,
      "iso-8601": "2021-10-03T11:49+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633250945655,
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
  "ipv4-address": "192.168.10.3",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": [
    {
      "uid": "5185f9ad-60e8-4812-b62a-616e0d1d97f7",
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
      "ipv4-address": "192.168.10.8",
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
