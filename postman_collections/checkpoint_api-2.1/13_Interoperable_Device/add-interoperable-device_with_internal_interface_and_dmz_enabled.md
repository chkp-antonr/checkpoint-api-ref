# add-interoperable-device with internal interface and dmz enabled

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interoperable-device`

## Description

Adds Interoperable Device with internal interface and dmz enabled

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
  "ip-address": "192.168.10.6",
  "interfaces.ip-address": "100.150.200.0",
  "interfaces.network-mask": "255.255.255.0",
  "interfaces.name": "internalInterface",
  "interfaces.topology-settings.interface-leads-to-dmz": "true",
  "interfaces.topology-settings.ip-address-behind-this-interface": "network defined by the interface ip and net mask"
}
```

## Example Responses

### Example 1: add-interoperable-device with internal interface and dmz enabled
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1754b78e-d91e-4ff5-997e-17d7f1a7b9e9",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.10.6",
  "interfaces": [
    {
      "uid": "04f543e8-09f7-48c3-a3c1-2b171d176a94",
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
      "anti-spoofing": true,
      "topology": "internal",
      "topology-settings": {
        "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
        "interface-leads-to-dmz": true
      },
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
      "posix": 1734178367916,
      "iso-8601": "2024-12-14T14:12+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734178367916,
      "iso-8601": "2024-12-14T14:12+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
