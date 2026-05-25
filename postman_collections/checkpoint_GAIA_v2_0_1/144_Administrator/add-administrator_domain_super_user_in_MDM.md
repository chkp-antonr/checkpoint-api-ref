# add-administrator (domain super user) in MDM

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
  "name": "super_admin",
  "password": "aaaa",
  "must-change-password": false,
  "email": "admin@gmail.com",
  "phone-number": "1800-800-800",
  "authentication-method": "check point password",
  "multi-domain-profile": "domain super user"
}
```

## Example Responses

### Example 1: add-administrator (domain super user) in MDM
**Status:** `200 OK`
