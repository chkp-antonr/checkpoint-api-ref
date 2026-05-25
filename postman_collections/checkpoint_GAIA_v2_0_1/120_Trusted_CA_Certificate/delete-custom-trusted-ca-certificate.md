# delete-custom-trusted-ca-certificate

**Collection:** Web API (version 2.0.1) > 120 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-custom-trusted-ca-certificate`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "f6afaa0f-f978-4b1c-8575-6cbc9459af11"
}
```

## Example Responses

### Example 1: delete-custom-trusted-ca-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
