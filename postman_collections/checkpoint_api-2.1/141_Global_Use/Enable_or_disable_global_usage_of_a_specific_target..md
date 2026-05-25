# Enable or disable global usage of a specific target.

**Collection:** Web API (version 2.1) > 141 Global Use
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-gateway-global-use`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "target": "vpn_gw",
  "enabled": true
}
```

## Example Responses

### Example 1: Enable or disable global usage of a specific target.
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5a4a8c10-7b17-49c9-b74f-6e564dca7a4c",
  "name": "vpn_gw",
  "type": "simple-gateway",
  "domain": {
    "uid": "39a5746e-921d-4498-8c8c-7763e6eb792b",
    "name": "dom1",
    "domain-type": "domain"
  },
  "enabled": true
}
```
