# add voip-domain-sip-proxy

**Collection:** Web API (version 2.1) > 25 VoIP Domain SIP Proxy
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-voip-domain-sip-proxy`

## Description

Add new voip domain sip proxy

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "sip1",
  "endpoints-domain": "new_group",
  "installed-at": "test_host"
}
```

## Example Responses

### Example 1: add voip-domain-sip-proxy
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "538b8046-d50c-4d09-93a4-92a7fe0329a5",
  "name": "sip1",
  "type": "voip-domain-sip-proxy",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753775945202,
      "iso-8601": "2025-07-29T10:59+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753775945202,
      "iso-8601": "2025-07-29T10:59+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/VoIPSIP",
  "endpoints-domain": {
    "uid": "ff1b4589-79d7-4e20-80f0-a0e356f4b291",
    "name": "new_group",
    "type": "group",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "General/group",
    "color": "black"
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
