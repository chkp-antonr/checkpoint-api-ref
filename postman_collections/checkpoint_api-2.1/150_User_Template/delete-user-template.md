# delete-user-template

**Collection:** Web API (version 2.1) > 150 User Template
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-user-template`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myusertemplate"
}
```

## Example Responses

### Example 1: delete-user-template
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
