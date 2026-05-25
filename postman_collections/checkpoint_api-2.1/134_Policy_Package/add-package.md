# add-package

**Collection:** Web API (version 2.1) > 134 Policy Package
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-package`

## Description

Add package

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_Standard_Package_1",
  "comments": "My Comments",
  "color": "green",
  "threat-prevention": false,
  "access": true
}
```

## Example Responses

### Example 1: add-package
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "00efec62-3534-4c28-be3a-feb9f4935ca6",
  "name": "New_Standard_Package_1",
  "type": "package",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1683557646294,
      "iso-8601": "2023-05-08T17:54+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1683557646294,
      "iso-8601": "2023-05-08T17:54+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "My Comments",
  "color": "light green",
  "icon": "Blades/Access",
  "access": true,
  "access-layers": [
    {
      "uid": "ef61148d-9a83-4495-a088-32bbfd18e182",
      "name": "New_Standard_Package_1 Network",
      "type": "access-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    }
  ],
  "vpn-traditional-mode": false,
  "nat-policy": true,
  "qos": false,
  "qos-policy-type": "recommended",
  "desktop-security": false,
  "threat-prevention": false,
  "installation-targets": "all",
  "https-inspection-policy": true,
  "https-inspection-layers": {
    "inbound-https-layer": {
      "uid": "7ec7bcea-3d84-4dde-9b4b-6a057845d26c",
      "name": "Default Inbound Layer",
      "type": "https-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    },
    "outbound-https-layer": {
      "uid": "97b6c38c-18a8-40d5-93fb-a114028f2dd6",
      "name": "Default Outbound Layer",
      "type": "https-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    }
  }
}
```
