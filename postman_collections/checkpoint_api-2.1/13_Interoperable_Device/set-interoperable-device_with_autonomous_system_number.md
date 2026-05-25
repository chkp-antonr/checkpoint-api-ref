# set-interoperable-device with autonomous system number

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-interoperable-device`

## Description

Sets Interoperable Device with a custom Autonomous System Number

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "InteroperableDevice",
  "asn": 65535
}
```

## Example Responses

### Example 1: set-interoperable-device with autonomous system number
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3b330a2b-d626-49c6-864a-2309a6d2957e",
  "name": "InteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.1.6",
  "interfaces": [
    {
      "uid": "504d613d-d9e5-4b19-a04a-8878ef7cf1fc",
      "name": "",
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
    "vpn-domain-type": "manual",
    "vpn-domain": "InteroperableDevice_Network_2",
    "vpn-domain-exclude-external-ip-addresses": false
  },
  "groups": [],
  "tags": [],
  "autonomous-system-number": "65535",
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734300029666,
      "iso-8601": "2024-12-16T00:00+0200"
    },
    "last-modifier": "aa",
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
