# delete securid-server

**Collection:** Web API (version 2.1) > 43 SecurID Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-securid-server`

## Description

Deletes SecureID server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSecurIdServer"
}
```

## Example Responses

### Example 1: delete securid-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
