# add-administrator

**Collection:** Web API (version 2.0.1) > 144 Administrator
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-administrator`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "admin",
  "password": "secret",
  "must-change-password": false,
  "email": "admin@gmail.com",
  "phone-number": "1800-800-800",
  "authentication-method": "check point password",
  "permissions-profile": "read write all"
}
```

## Example Responses

### Example 1: add-administrator
**Status:** `200 OK`
