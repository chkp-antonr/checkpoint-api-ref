# delete-access-point-name

**Collection:** Web API (version 2.0.1) > 22 Access Point Name
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-access-point-name`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myaccesspointname"
}
```

## Example Responses

### Example 1: delete-access-point-name
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
