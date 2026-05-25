# set idp-to-domain-assignment of domain to use default idp-to-domain-assignment

**Collection:** Web API (version 2.1) > 161 Identity Provider To Domain Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-idp-to-domain-assignment`

## Description

set idp-to-domain-assignment of domain to use default idp-to-domain-assignment

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "assigned-domain": "BSMS",
  "using-default": "true"
}
```

## Example Responses

### Example 1: set idp-to-domain-assignment of domain to use default idp-to-domain-assignment
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "fe866287-248a-4fb3-9e5e-bb0e1ac90788",
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
      "posix": 1642087856621,
      "iso-8601": "2022-01-13T17:30+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1641462834333,
      "iso-8601": "2022-01-06T11:53+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": true,
  "identity-provider-set": false,
  "using-default": true,
  "assigned-domain": {
    "uid": "e6e6cc24-9881-4869-975c-7b3ac8d4347d",
    "name": "BSMS",
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
