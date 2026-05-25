# show-vpn-communities-remote-access (with override vpn domains)

**Collection:** Web API (version 2.1) > 109 VPN Community Remote Access
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-vpn-communities-remote-access`

## Description

Displays several remote access VPN communities with override VPN domains.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full"
}
```

## Example Responses

### Example 1: show-vpn-communities-remote-access (with override vpn domains)
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "6cccf348-4807-4d55-83bd-55a4192746a1",
      "name": "RemoteAccess",
      "type": "vpn-community-remote-access",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "VPNCommunities/Remote",
      "color": "black"
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
