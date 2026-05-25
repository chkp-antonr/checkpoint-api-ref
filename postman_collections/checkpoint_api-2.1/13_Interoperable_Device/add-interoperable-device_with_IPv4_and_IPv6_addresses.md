# add-interoperable-device with IPv4 and IPv6 addresses

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-interoperable-device`

## Description

Adds Interoperable Device with IPv4 and IPv6 addresses

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "NewInteroperableDevice",
  "ipv4-address": "192.168.1.6",
  "ipv6-address": "2001:0db8:85a3:0000:0000:8a2e:0370:7334"
}
```

## Example Responses

### Example 1: add-interoperable-device with IPv4 and IPv6 addresses
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "51c4bd59-d7f8-4df9-a1c9-9145383458d1",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "ipv4-address": "192.168.1.6",
  "ipv6-address": "2001:db8:85a3::8a2e:370:7334",
  "interfaces": [],
  "vpn-settings": {
    "vpn-domain-type": "addresses_behind_gw",
    "vpn-domain-exclude-external-ip-addresses": false
  },
  "groups": [],
  "tags": [],
  "autonomous-system-number": "0",
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1734178471974,
      "iso-8601": "2024-12-14T14:14+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734178471974,
      "iso-8601": "2024-12-14T14:14+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
    "clone": "not_supported"
  }
}
```
