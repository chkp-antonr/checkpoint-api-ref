# clone-access-role

**Collection:** Web API (version 2.1) > 148 Access Role
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-access-role`

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

### Example 1: clone-access-role
**Status:** `200 OK`
