# set-login-restrictions

**Collection:** Web API (version 2.1) > 168 Login Restrictions
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-login-restrictions`

## Description

Edit login restrictions.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "lockout-admin-account": true,
  "failed-authentication-attempts": 10,
  "unlock-admin-account": false,
  "lockout-duration": 30,
  "display-access-denied-message": false
}
```

## Example Responses

### Example 1: set-login-restrictions
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f598023d-2ace-482d-aec6-c5cf536e08ad",
  "type": "login-restrictions",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1738766276949,
      "iso-8601": "2025-02-05T16:37+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1738588308605,
      "iso-8601": "2025-02-03T15:11+0200"
    },
    "creator": "System"
  },
  "lockout-admin-account": true,
  "failed-authentication-attempts": 10,
  "unlock-admin-account": false,
  "lockout-duration": 30,
  "display-access-denied-message": false
}
```
