# add-access-role

**Collection:** Web API (version 2.0.1) > 137 Access Role
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-access-role`

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
  "networks": "any",
  "users": "any",
  "machines": "all identified",
  "remote-access-clients": "any"
}
```

## Example Responses

### Example 1: add-access-role
**Status:** `200 OK`
