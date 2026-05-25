# set-interoperable-device with a different vpn-domain

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Sets Interoperable Device with a different vpn-domain option

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
  "vpn-settings.vpn-domain-type": "manual",
  "vpn-settings.vpn-domain": "InteroperableDevice_Network_2"
}
```

## Example Responses

### Example 1: set-interoperable-device with a different vpn-domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4fa631c7-46f5-479a-9b81-d39277056e50",
  "name": "NewInteroperableDevice",
  "type": "interop",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1630497573291,
      "iso-8601": "2021-09-01T14:59+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1630495698947,
      "iso-8601": "2021-09-01T14:28+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.1.6",
  "ipv6-address": "2001:db8:85a3::8a2e:370:7334",
  "vpn-settings": {
    "vpn-domain-type": "manual",
    "vpn-domain": "InteroperableDevice_Network_2"
  },
  "interfaces": []
}
```
