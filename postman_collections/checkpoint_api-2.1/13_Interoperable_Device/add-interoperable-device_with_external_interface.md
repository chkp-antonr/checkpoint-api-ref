# add-interoperable-device with external interface

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interoperable-device`

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
  "uid": "daee4df5-c595-4c8c-85d1-8cc10f69e2cc",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.10.2",
  "interfaces": [
    {
      "uid": "e3b0d043-a616-4078-a049-62410ef967cd",
      "name": "externalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address": "91.90.143.5",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "anti-spoofing": true,
      "topology": "external",
      "anti-spoofing-settings": {
        "action": "prevent",
        "exclude-packets": false,
        "spoof-tracking": "log"
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
      "posix": 1734178257409,
      "iso-8601": "2024-12-14T14:10+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734178257409,
      "iso-8601": "2024-12-14T14:10+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
