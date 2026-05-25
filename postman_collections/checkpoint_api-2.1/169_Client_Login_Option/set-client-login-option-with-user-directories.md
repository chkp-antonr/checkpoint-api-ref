# set-client-login-option-with-user-directories

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
  "name": "my-client-login-option",
  "user-directories": {
    "configuration-mode": "manual",
    "manual-configuration": {
      "internal-users": true,
      "external-user-profiles": true,
      "ldap-users": false
    }
  }
}
```

## Example Responses

### Example 1: set-client-login-option-with-user-directories
**Status:** `200 OK`
