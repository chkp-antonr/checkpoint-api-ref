# delete-limit

**Collection:** Web API (version 2.1) > 186 Limit
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-limit`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "limit_obj_Clone"
}
```

## Example Responses

### Example 1: delete-limit
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
