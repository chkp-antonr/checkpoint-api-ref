# set voip-domain-mgcp-call-agent

**Collection:** Web API (version 2.1) > 26 VoIP Domain MGCP Call Agent
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-voip-domain-mgcp-call-agent`

## Description

Edits end point of voip domain mgcp call agent.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mgcp1",
  "endpoints-domain": "IPv6_Link_Local_Hosts"
}
```

## Example Responses

### Example 1: set voip-domain-mgcp-call-agent
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "17d1a265-0eb9-4bfe-8b9c-031cac81aced",
  "name": "mgcp1",
  "type": "voip-domain-mgcp-call-agent",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753775713497,
      "iso-8601": "2025-07-29T10:55+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753775541926,
      "iso-8601": "2025-07-29T10:52+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/VoIPMGCPCallAgent",
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
