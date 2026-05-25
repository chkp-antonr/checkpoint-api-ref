# set-client-login-option-remove-authentication-method

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
  "name": "multivalue-test-clo",
  "authentication-methods": {
    "remove": {
      "0": {
        "authentication-factor": "username-and-password"
      }
    }
  }
}
```

## Example Responses

### Example 1: set-client-login-option-remove-authentication-method
**Status:** `200 OK`
