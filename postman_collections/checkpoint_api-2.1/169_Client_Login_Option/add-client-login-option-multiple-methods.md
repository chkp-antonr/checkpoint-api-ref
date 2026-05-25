# add-client-login-option-multiple-methods

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
  "name": "enterprise-mixed-auth",
  "authentication-methods": [
    {
      "authentication-factor": "personal-certificate"
    },
    {
      "authentication-factor": "radius",
      "radius-server": "corp-radius-server"
    },
    {
      "authentication-factor": "username-and-password"
    }
  ]
}
```

## Example Responses

### Example 1: add-client-login-option-multiple-methods
**Status:** `200 OK`
