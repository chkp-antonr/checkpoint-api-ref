# delete-service-tcp

**Collection:** Web API (version 2.0.1) > 68 Service TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-service-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_TCP_Service_1"
}
```

## Example Responses

### Example 1: delete-service-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
