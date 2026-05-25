# show voip-domain-h323-gatekeeper

**Collection:** Web API (version 2.1) > 28 VoIP Domain H.323 Gatekeeper
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-h323-gatekeeper`

## Description

Show existing voip domain h323 gatekeeper

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vdhg1"
}
```

## Example Responses

### Example 1: show voip-domain-h323-gatekeeper
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6b5beb1d-8332-4cf8-b7f8-4598bbb2c10d",
  "name": "vdhg1",
  "type": "voip-domain-h323-gatekeeper",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753952854653,
      "iso-8601": "2025-07-31T12:07+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1753952854653,
      "iso-8601": "2025-07-31T12:07+0300"
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
  "icon": "NetworkObjects/VoIPGatekeeper",
  "endpoints-domain": {
    "uid": "8606c272-3307-4c2d-ab09-37892959492f",
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
    "direct": true,
    "call-setup": false,
    "call-setup-and-call-control": false
  }
}
```
