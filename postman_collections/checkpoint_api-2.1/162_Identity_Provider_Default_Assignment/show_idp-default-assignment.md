# show idp-default-assignment

**Collection:** Web API (version 2.1) > 162 Identity Provider Default Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-idp-default-assignment`

## Description

show idp-default-assignment

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show idp-default-assignment
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
      "posix": 1642087739545,
      "iso-8601": "2022-01-13T17:28+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1641202839199,
      "iso-8601": "2022-01-03T11:40+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": false,
  "identity-provider-set": false
}
```
