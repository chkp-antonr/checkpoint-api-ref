# add-passcode-profile

**Collection:** Web API (version 2.0.1) > 86 Passcode Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-passcode-profile`

## Description

Adds a new Passcode Profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New App Passcode Policy"
}
```

## Example Responses

### Example 1: add-passcode-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6e5a4445-8c6a-4742-a505-b9b035fb1977",
  "name": "New App Passcode Policy",
  "type": "passcode_profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1651647509215,
      "iso-8601": "2022-05-04T09:58+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1651647509215,
      "iso-8601": "2022-05-04T09:58+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa",
  "allow-simple-passcode": true,
  "enable-inactivity-time-lock": false,
  "enable-passcode-expiration": false,
  "enable-passcode-failed-attempts": false,
  "enable-passcode-history": false,
  "max-inactivity-time-lock": 15,
  "max-passcode-failed-attempts": 4,
  "min-passcode-complex-characters": 0,
  "min-passcode-length": 4,
  "passcode-expiration-period": 90,
  "passcode-history": 8,
  "require-alphanumeric-passcode": false
}
```
