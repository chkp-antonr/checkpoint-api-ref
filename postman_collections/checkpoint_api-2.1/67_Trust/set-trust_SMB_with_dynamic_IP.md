# set-trust SMB with dynamic IP

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
  "name": "smb_daip",
  "GW": true,
  "one-time-password": "aaaa",
  "trust-settings": {
    "initiation-phase": "when_gateway_connects",
    "identification-method": "mac_address",
    "gateway-mac-address": "ffff:45:0000:0000:0000"
  }
}
```

## Example Responses

### Example 1: set-trust SMB with dynamic IP
**Status:** `200 OK`

**Body:**
```javascript
{
  "name": "smb_daip",
  "trust-method": "one-time-password",
  "sic-state": "waiting_for_first_connection",
  "trust-details": {
    "identification-method": "mac_address",
    "gateway-mac-address": "ffff:45:0000:0000:0000"
  }
}
```
