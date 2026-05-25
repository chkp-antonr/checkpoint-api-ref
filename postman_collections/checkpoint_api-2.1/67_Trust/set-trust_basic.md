# set-trust basic

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
  "one-time-password": "aaaa"
}
```

## Example Responses

### Example 1: set-trust basic
**Status:** `200 OK`

**Body:**
```javascript
{
  "name": "gw1",
  "ipv4-address": "192.0.2.100",
  "trust-method": "one-time-password",
  "sic-state": "communicating"
}
```
