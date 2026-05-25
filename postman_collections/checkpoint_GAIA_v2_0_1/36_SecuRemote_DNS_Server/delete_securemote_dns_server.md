# delete securemote dns server

**Collection:** Web API (version 2.0.1) > 36 SecuRemote DNS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-securemote-dns-server`

## Description

Delete existing Securemote DNS server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSecuRemoteDNSSever"
}
```

## Example Responses

### Example 1: delete securemote dns server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
