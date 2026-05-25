# set-passcode-profile

**Collection:** Web API (version 2.1) > 97 Passcode Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-passcode-profile`

## Description

Setting Passcode profile object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New App Passcode Policy",
  "allow-simple-passcode": "true",
  "max-inactivity-time-lock": "30",
  "require-alphanumeric-passcode": "false"
}
```

## Example Responses

### Example 1: set-passcode-profile
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
      "posix": 1651648329644,
      "iso-8601": "2022-05-04T10:12+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1651647509222,
      "iso-8601": "2022-05-04T09:58+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "MobileProfile/passcode_policy",
  "allow-simple-passcode": true,
  "enable-inactivity-time-lock": false,
  "enable-passcode-expiration": false,
  "enable-passcode-failed-attempts": false,
  "enable-passcode-history": false,
  "max-inactivity-time-lock": 30,
  "max-passcode-failed-attempts": 4,
  "min-passcode-complex-characters": 0,
  "min-passcode-length": 4,
  "passcode-expiration-period": 90,
  "passcode-history": 8,
  "require-alphanumeric-passcode": false
}
```
