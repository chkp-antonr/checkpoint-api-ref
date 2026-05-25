# show idp-to-domain-assignment of domain

**Collection:** Web API (version 2.0.1) > 150 Identity Provider To Domain Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-idp-to-domain-assignment`

## Description

show idp-to-domain-assignment of domain

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "assigned-domain": "SMS"
}
```

## Example Responses

### Example 1: show idp-to-domain-assignment of domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2feed858-373b-4618-ae03-84e1a08bad72",
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
      "posix": 1642078321824,
      "iso-8601": "2022-01-13T14:52+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1641229065206,
      "iso-8601": "2022-01-03T18:57+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": false,
  "identity-provider-set": false,
  "using-default": true,
  "assigned-domain": {
    "uid": "8ecf2426-268d-44c6-95c6-85289d34318f",
    "name": "SMS",
    "type": "domain",
    "domain": {
      "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
      "name": "System Data",
      "domain-type": "mds"
    },
    "icon": "Objects/domain",
    "color": "black"
  }
}
```
