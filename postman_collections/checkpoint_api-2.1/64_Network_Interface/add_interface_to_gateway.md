# add interface to gateway

**Collection:** Web API (version 2.1) > 64 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interface`

## Description

Add network interface to gateway.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "gateway-uid": "ff918e85-98c4-4b17-bcac-417aab863d87",
  "ipv4-address": "11.1.1.1",
  "ipv4-mask-length": 24,
  "name": "eth0",
  "anti-spoofing-settings": {
    "action": "prevent",
    "exclude-packets": false,
    "spoof-tracking": "log"
  },
  "security-zone-settings": {
    "auto-calculated": false,
    "specific-zone": "ExternalZone",
    "auto-calculated-zone": "InternalZone",
    "specific-security-zone-enabled": true
  },
  "topology-settings": {
    "interface-leads-to-dmz": false,
    "ip-address-behind-this-interface": "not defined"
  },
  "topology": "external",
  "anti-spoofing": true
}
```

## Example Responses

### Example 1: add interface to gateway
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f400bd09-381f-4435-b8f4-9e13338c6ad6",
  "name": "eth0",
  "type": "interface",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "topology-settings-automatic": {
    "ip-address-behind-this-interface": "not defined",
    "interface-leads-to-dmz": false
  },
  "topology-automatic": "internal",
  "topology-manual": "external",
  "topology-settings-manual": {
    "ip-address-behind-this-interface": "not defined",
    "interface-leads-to-dmz": false
  },
  "anti-spoofing-settings": {
    "action": "prevent",
    "exclude-packets": false,
    "spoof-tracking": "log"
  },
  "network-interface-type": "ethernet",
  "security-zone-settings": {
    "auto-calculated-zone": "InternalZone",
    "auto-calculated-zone-uid": "e8131db2-8388-42a5-924a-82de32db20f7",
    "specific-zone-uid": "237a4cbc-7fb6-4d50-872a-4904468271c4",
    "specific-security-zone-enabled": true,
    "auto-calculated": false,
    "specific-zone": "ExternalZone"
  },
  "anti-spoofing": true,
  "ipv4-address": "11.1.1.1",
  "ipv4-mask-length": 24,
  "gateway": {
    "type": "simple-gateway",
    "name": "dummy-gw-1",
    "uid": "ff918e85-98c4-4b17-bcac-417aab863d87"
  },
  "comments": "",
  "color": "black",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1685343305437,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1685343305189,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "creator": "aa"
  },
  "read-only": true,
  "available-actions": {}
}
```
