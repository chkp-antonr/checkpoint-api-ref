# show network interface

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interface`

## Description

Show network interface.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "f400bd09-381f-4435-b8f4-9e13338c6ad6"
}
```

## Example Responses

### Example 1: show network interface
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
  "topology-manual": "internal",
  "topology-settings-manual": {
    "ip-address-behind-this-interface": "not defined",
    "interface-leads-to-dmz": false
  },
  "anti-spoofing-settings": {
    "action": "detect",
    "exclude-packets": false,
    "spoof-tracking": "alert"
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
  "anti-spoofing": false,
  "ipv4-address": "1.12.33.11",
  "ipv4-mask-length": 21,
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
      "posix": 1685343307386,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1685343305189,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "creator": "aa"
  },
  "read-only": false,
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  }
}
```
