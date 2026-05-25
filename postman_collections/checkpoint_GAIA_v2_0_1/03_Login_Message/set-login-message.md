# set-login-message

**Collection:** Web API (version 2.0.1) > 03 Login Message
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-login-message`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "show-message": "true",
  "header": "Warning",
  "message": "Unauthorized access of this server is prohibited and punished by law",
  "warning": "true"
}
```

## Example Responses

### Example 1: set-login-message
**Status:** `200 OK`
