# add-interoperable-device with vpn-domain

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interoperable-device`

## Description

Adds Interoperable Device with vpn-domain option

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
  "ip-address": "192.168.1.6",
  "vpn-settings.vpn-domain-type": "manual",
  "vpn-settings.vpn-domain": "InteroperableDevice_Network_1"
}
```

## Example Responses

### Example 1: add-interoperable-device with vpn-domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3eeb3541-46eb-48e9-a122-53a8895c1ed8",
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
      "posix": 1630479385463,
      "iso-8601": "2021-09-01T09:56+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1630479385463,
      "iso-8601": "2021-09-01T09:56+0300"
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
  "ipv6-address": "",
  "vpn-settings": {
    "vpn-domain-type": "manual",
    "vpn-domain": "InteroperableDevice_Network_1"
  },
  "interfaces": []
}
```
