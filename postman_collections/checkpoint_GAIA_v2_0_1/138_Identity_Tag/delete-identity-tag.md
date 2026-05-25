# delete-identity-tag

**Collection:** Web API (version 2.0.1) > 138 Identity Tag
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-identity-tag`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myidentitytag"
}
```

## Example Responses

### Example 1: delete-identity-tag
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
