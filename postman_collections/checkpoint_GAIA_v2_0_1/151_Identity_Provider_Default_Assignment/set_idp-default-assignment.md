# set idp-default-assignment

**Collection:** Web API (version 2.0.1) > 151 Identity Provider Default Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-idp-default-assignment`

## Description

set idp default assignment

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "identity-provider": "azure"
}
```

## Example Responses

### Example 1: set idp-default-assignment
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ed31002e-6738-4047-b406-c3640709a5de",
  "type": "idp-to-domain-assignment",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1642087771073,
      "iso-8601": "2022-01-13T17:29+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1641202839199,
      "iso-8601": "2022-01-03T11:40+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": true,
  "identity-provider": {
    "uid": "471c3e86-8edd-4fc1-bc7f-38678346f748",
    "name": "azure",
    "type": "CpmiIdentityProviderMirror",
    "domain": {
      "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
      "name": "System Data",
      "domain-type": "mds"
    },
    "icon": "Objects/AuthenticationServer",
    "color": "black"
  },
  "identity-provider-set": true
}
```
