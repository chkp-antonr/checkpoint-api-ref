# add-interoperable-device with default interface

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interoperable-device`

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
  "uid": "241c8eab-0f91-4970-a793-a53f0c6c7b5e",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.10.1",
  "interfaces": [
    {
      "uid": "3310710e-1e0a-4ebd-9332-0adb244d950c",
      "name": "internalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address": "100.150.200.0",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "anti-spoofing": false,
      "topology": "internal",
      "topology-settings": {
        "ip-address-behind-this-interface": "not defined",
        "interface-leads-to-dmz": false
      },
      "tags": [],
      "comments": "",
      "color": "black",
      "icon": "Unknown"
    }
  ],
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
      "posix": 1734178198471,
      "iso-8601": "2024-12-14T14:09+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734178198471,
      "iso-8601": "2024-12-14T14:09+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
