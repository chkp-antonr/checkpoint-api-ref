# Generate cloud token (Smart-1-Cloud)

**Collection:** Web API (version 2.1) > 67 Trust
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-trust`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
  "trust-method": "cloud_token"
}
```

## Example Responses

### Example 1: Generate cloud token (Smart-1-Cloud)
**Status:** `200 OK`

**Body:**
```javascript
{
  "name": "gw1",
  "ipv4-address": "192.0.2.230",
  "trust-method": "cloud_token",
  "sic-state": "uninitialized",
  "trust-details": {
    "status": "uninitialized",
    "authentication-token": "aHR0...4Y2",
    "token-expiration-date": "2025-09-09T09:43:44.465Z",
    "cloud-communication-details": {
      "ip": "100.100.12.2",
      "status": "token_issued"
    }
  }
}
```
