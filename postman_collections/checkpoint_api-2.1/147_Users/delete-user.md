# delete-user

**Collection:** Web API (version 2.1) > 147 Users
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-user`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myuser"
}
```

## Example Responses

### Example 1: delete-user
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
