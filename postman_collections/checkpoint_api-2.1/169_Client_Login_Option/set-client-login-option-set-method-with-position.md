# set-client-login-option-set-method-with-position

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
    "0": {
      "authentication-factor": "username-and-password",
      "position": 1
    }
  }
}
```

## Example Responses

### Example 1: set-client-login-option-set-method-with-position
**Status:** `200 OK`
