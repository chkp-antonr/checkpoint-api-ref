# clone voip-domain-sccp-call-manager

**Collection:** Web API (version 2.1) > 27 VoIP Domain SCCP Call Manager
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-voip-domain-sccp-call-manager`

## Description

Clone voip domain voip domain sccp call manager.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "sccp1",
  "endpoints-domain": "IPv6_Link_Local_Hosts"
}
```

## Example Responses

### Example 1: clone voip-domain-sccp-call-manager
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "08411e0b-2c25-4fbd-bbed-790925396207",
  "name": "sccp1_Clone",
  "type": "voip-domain-sccp-call-manager",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753777106188,
      "iso-8601": "2025-07-29T11:18+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753777106188,
      "iso-8601": "2025-07-29T11:18+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/VoIPSCCPCallManager",
  "endpoints-domain": {
    "uid": "caee1116-8087-4310-9208-b422d3628a7e",
    "name": "IPv6_Link_Local_Hosts",
    "type": "network",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "NetworkObjects/network",
    "color": "black",
    "subnet6": "fe80::",
    "mask-length6": 64
  },
  "installed-at": {
    "uid": "a7a5866b-ec76-48a1-9e70-73fd1c85b8a0",
    "name": "test_host",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "2.3.4.5"
  }
}
```
