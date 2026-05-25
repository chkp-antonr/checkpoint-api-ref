# add-basic-client-login-option

**Collection:** Web API (version 2.1) > 169 Client Login Option
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-client-login-option`

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
      "authentication-factor": "username-and-password"
    }
  }
}
```

## Example Responses

### Example 1: add-basic-client-login-option
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a364661f-3695-4283-b317-4ea9e7ea0946",
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
      "posix": 1762075472536,
      "iso-8601": "2025-11-02T11:24+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1762075472536,
      "iso-8601": "2025-11-02T11:24+0200"
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
      "authentication-factor": "username-and-password"
    }
  ],
  "user-directories": {
    "configuration-mode": "automatic",
    "manual-configuration": {
      "internal-users": true,
      "external-user-profiles": false,
      "ldap-users": false,
      "ldap-scope": "all-gateway-directories"
    },
    "ldap-lookup-type": "according-to-ldap-account-unit-profile"
  }
}
```
