# add-interoperable-device with internal interface and dmz enabled

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

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
  "uid": "aa61268d-47f3-4c21-904e-6b773aa43ee3",
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
      "posix": 1633245403439,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633245403439,
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
  "ipv4-address": "192.168.10.6",
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw"
  },
  "interfaces": [
    {
      "uid": "d7f3dcd0-a0e8-4cb1-8365-200115bd2a2a",
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
        "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
        "interface-leads-to-dmz": true
      },
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
