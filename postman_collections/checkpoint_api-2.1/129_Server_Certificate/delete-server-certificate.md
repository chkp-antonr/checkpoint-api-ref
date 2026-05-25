# delete-server-certificate

**Collection:** Web API (version 2.1) > 129 Server Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-server-certificate`

## Description

Delete a server certificate object.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "MyServerCertificate"
}
```

## Example Responses

### Example 1: delete-server-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
