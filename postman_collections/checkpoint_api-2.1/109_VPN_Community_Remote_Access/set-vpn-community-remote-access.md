# set-vpn-community-remote-access

**Collection:** Web API (version 2.1) > 109 VPN Community Remote Access
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-remote-access`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "user-groups": [
    "myusergroup"
  ],
  "gateways": [
    "mygateway"
  ]
}
```

## Example Responses

### Example 1: set-vpn-community-remote-access
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "21ba3e65-f6ef-4e81-b2f5-129ba65b890c",
  "name": "RemoteAccess",
  "type": "vpn-community-remote-access",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "VPNCommunities/Remote",
  "gateways": [
    {
      "uid": "9965eb0f-4945-4be6-8a4c-424865022ad0",
      "name": "mygateway",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "user-groups": [
    {
      "uid": "3f829b4f-0380-476c-9227-ac074ead1470",
      "name": "myusergroup",
      "type": "user-group",
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
