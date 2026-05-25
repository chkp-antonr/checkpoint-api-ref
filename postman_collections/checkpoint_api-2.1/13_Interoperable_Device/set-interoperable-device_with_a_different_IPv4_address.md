# set-interoperable-device with a different IPv4 address

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-interoperable-device`

## Description

Sets Interoperable Device with a different IPv4 address

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

### Example 1: set-interoperable-device with a different IPv4 address
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3b330a2b-d626-49c6-864a-2309a6d2957e",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.1.6",
  "interfaces": [
    {
      "uid": "2328c01a-c3eb-47d1-bf90-1a61d9589f94",
      "name": "externalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address": "100.170.200.0",
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
      "posix": 1734275555031,
      "iso-8601": "2024-12-15T17:12+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734275245188,
      "iso-8601": "2024-12-15T17:07+0200"
    },
    "creator": "aa"
  },
  "read-only": false,
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "not_supported"
  }
}
```
