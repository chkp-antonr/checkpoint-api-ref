# show voip-domain-sccp-call-manager

**Collection:** Web API (version 2.1) > 27 VoIP Domain SCCP Call Manager
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-sccp-call-manager`

## Description

Shows voip domain sccp call manager.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "sccp1"
}
```

## Example Responses

### Example 1: show voip-domain-sccp-call-manager
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "02865dda-4985-4182-b528-5f7b25a43c66",
  "name": "sccp1",
  "type": "voip-domain-sccp-call-manager",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753776654165,
      "iso-8601": "2025-07-29T11:10+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753776654165,
      "iso-8601": "2025-07-29T11:10+0300"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/VoIPSCCPCallManager",
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
