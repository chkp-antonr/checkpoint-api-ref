# clone voip-domain-h323-gateway

**Collection:** Web API (version 2.1) > 29 VoIP Domain H.323 Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-voip-domain-h323-gateway`

## Description

Clone voip domain h323 gateway.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vdhgw1",
  "endpoints-domain": "IPv6_Link_Local_Hosts"
}
```

## Example Responses

### Example 1: clone voip-domain-h323-gateway
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2972a79c-6b90-4875-a528-8c1826450804",
  "name": "vdhgw1_Clone",
  "type": "voip-domain-h323-gateway",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753953215236,
      "iso-8601": "2025-07-31T12:13+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753953215236,
      "iso-8601": "2025-07-31T12:13+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/VoIPGateway",
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
    "uid": "45e8835e-9522-428d-bf12-d22baaa84609",
    "name": "test_host",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "1.1.1.1"
  },
  "routing-mode": {
    "call-setup": true,
    "call-setup-and-call-control": false
  }
}
```
