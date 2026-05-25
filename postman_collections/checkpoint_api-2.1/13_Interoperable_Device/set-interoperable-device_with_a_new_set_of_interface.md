# set-interoperable-device with a new set of interface

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-interoperable-device`

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
  "uid": "3b330a2b-d626-49c6-864a-2309a6d2957e",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.1.6",
  "ipv6-address": "2001:db8:85a3::8a2e:370:7334",
  "interfaces": [
    {
      "uid": "504d613d-d9e5-4b19-a04a-8878ef7cf1fc",
      "name": "internalInterface",
      "type": "CpmiInterface",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address": "192.168.10.8",
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
      "posix": 1734299655781,
      "iso-8601": "2024-12-15T23:54+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734275245188,
      "iso-8601": "2024-12-15T17:07+0200"
    },
    "creator": "aa"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
