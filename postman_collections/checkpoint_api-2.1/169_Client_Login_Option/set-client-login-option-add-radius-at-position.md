# set-client-login-option-add-radius-at-position

**Collection:** Web API (version 2.1) > 169 Client Login Option
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-client-login-option`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "basic-clo",
  "authentication-methods": {
    "0": {
      "authentication-factor": "radius",
      "position": 1,
      "radius": {
        "server": "radius-server"
      }
    }
  }
}
```

## Example Responses

### Example 1: set-client-login-option-add-radius-at-position
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2343635e-9dad-4e94-834e-4ad65de520c3",
  "name": "basic-clo",
  "type": "client-login-option",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1764238929549,
      "iso-8601": "2025-11-27T12:22+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1764238658228,
      "iso-8601": "2025-11-27T12:17+0200"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa",
  "display-name": "New Login Option",
  "authentication-methods": [
    {
      "authentication-factor": "radius",
      "radius": {
        "server": {
          "uid": "71724469-7639-4924-a70b-91283aaf074f",
          "name": "malky",
          "type": "radius-server",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "Objects/account_unit",
          "color": "black"
        },
        "ask-user-password": true
      }
    }
  ],
  "user-directories": {
    "configuration-mode": "automatic",
    "manual-configuration": {
      "internal-users": false,
      "external-user-profiles": false,
      "ldap-users": false,
      "ldap-scope": "all-gateway-directories"
    },
    "ldap-lookup-type": "according-to-ldap-account-unit-profile"
  }
}
```
