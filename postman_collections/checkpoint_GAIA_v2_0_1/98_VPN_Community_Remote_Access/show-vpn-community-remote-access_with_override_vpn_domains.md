# show-vpn-community-remote-access (with override vpn domains)

**Collection:** Web API (version 2.0.1) > 98 VPN Community Remote Access
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-vpn-community-remote-access`

## Description

Displays remote access VPN community with override VPN domains.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "RemoteAccess"
}
```

## Example Responses

### Example 1: show-vpn-community-remote-access (with override vpn domains)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6cccf348-4807-4d55-83bd-55a4192746a1",
  "name": "RemoteAccess",
  "type": "vpn-community-remote-access",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1735537446959,
      "iso-8601": "2024-12-30T07:44+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734364949807,
      "iso-8601": "2024-12-16T18:02+0200"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "false",
    "clone": "not_supported"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "VPNCommunities/Remote",
  "override-vpn-domains": [
    {
      "gateway": {
        "uid": "cfa0d682-6998-4c01-a4bd-0ef6c400a09a",
        "name": "gw1",
        "type": "simple-gateway",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      },
      "vpn-domain": {
        "uid": "72ad896c-e810-4824-90ee-ae6474f5d9f8",
        "name": "CP_default_Office_Mode_addresses_pool",
        "type": "network",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/network",
        "color": "black",
        "subnet4": "172.16.10.0",
        "subnet-mask": "255.255.255.0",
        "mask-length4": 24
      }
    }
  ],
  "gateways": [
    {
      "uid": "cfa0d682-6998-4c01-a4bd-0ef6c400a09a",
      "name": "gw1",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    }
  ],
  "user-groups": [
    {
      "uid": "97aeb36a-9aeb-11d5-bd16-0090272ccb30",
      "name": "All Users",
      "type": "CpmiAnyObject",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "General/globalsAny",
      "color": "black"
    }
  ]
}
```
