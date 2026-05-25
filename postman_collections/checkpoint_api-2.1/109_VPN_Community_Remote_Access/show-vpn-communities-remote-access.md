# show-vpn-communities-remote-access

**Collection:** Web API (version 2.1) > 109 VPN Community Remote Access
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-vpn-communities-remote-access`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-vpn-communities-remote-access
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "21ba3e65-f6ef-4e81-b2f5-129ba65b890c",
      "name": "RemoteAccess",
      "type": "vpn-community-remote-access",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "route-based-settings": {
    "add-automatic-routes": "bgp",
    "override-routes": [],
    "advanced": {
      "bfd": false,
      "graceful-restart": true
    }
  }
}
```
