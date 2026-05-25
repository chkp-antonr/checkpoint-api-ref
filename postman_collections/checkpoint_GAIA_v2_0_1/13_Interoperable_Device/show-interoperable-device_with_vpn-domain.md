# show-interoperable-device with vpn-domain

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interoperable-device`

## Description

Shows an Interoperable Device with vpn-domain

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "NewInteroperableDevice"
}
```

## Example Responses

### Example 1: show-interoperable-device with vpn-domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "22006a76-9d77-4e9c-8db0-2ba7fe48a224",
  "name": "NewInteroperableDevice",
  "type": "interoperable-device",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1633245402464,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1633245402464,
      "iso-8601": "2021-10-03T10:16+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "192.168.5.6",
  "vpn-settings": {
    "vpn-domain-type": "manual",
    "vpn-domain": "InteroperableDevice_Network_1"
  },
  "interfaces": []
}
```
