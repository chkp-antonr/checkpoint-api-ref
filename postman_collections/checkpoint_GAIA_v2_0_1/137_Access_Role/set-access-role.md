# set-access-role

**Collection:** Web API (version 2.0.1) > 137 Access Role
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-access-role`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Access Role 1",
  "users": "all identified",
  "machines": "any"
}
```

## Example Responses

### Example 1: set-access-role
**Status:** `200 OK`
