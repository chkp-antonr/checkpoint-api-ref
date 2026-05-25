# set-administrator

**Collection:** Web API (version 2.0.1) > 144 Administrator
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-administrator`

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
  "password": "bew secret",
  "permissions-profile": "read only profile"
}
```

## Example Responses

### Example 1: set-administrator
**Status:** `200 OK`
