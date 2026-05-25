# delete-service-icmp

**Collection:** Web API (version 2.1) > 81 Service ICMP
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-service-icmp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "icmp3"
}
```

## Example Responses

### Example 1: delete-service-icmp
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
