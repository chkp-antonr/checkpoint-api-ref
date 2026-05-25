# delete-dns-domain

**Collection:** Web API (version 2.1) > 20 DNS Domain
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-dns-domain`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": ".example.com"
}
```

## Example Responses

### Example 1: delete-dns-domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
