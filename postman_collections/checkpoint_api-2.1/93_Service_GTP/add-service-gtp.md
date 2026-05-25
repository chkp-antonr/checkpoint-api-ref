# add-service-gtp

**Collection:** Web API (version 2.1) > 93 Service GTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-gtp`

## Description

Add GTP Service

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_gtp_Service_1",
  "version": "V2",
  "reverse-service": false,
  "imsi-prefix": {
    "enable": true,
    "prefix": "313460000000001"
  },
  "selection-mode": {
    "enable": true,
    "mode": 2
  },
  "trace-management": true
}
```

## Example Responses

### Example 1: add-service-gtp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "70e390d7-b070-4d6e-b8d7-53b7f6cc7fe6",
  "name": "New_gtp_Service_1",
  "type": "service-gtp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1587897335598,
      "iso-8601": "2020-04-26T13:35+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1587897335598,
      "iso-8601": "2020-04-26T13:35+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/GTPService",
  "groups": [],
  "version": "v2",
  "reverse-service": false,
  "interface-profile": {
    "profile": {
      "uid": "b458696d-8967-469c-91cc-c6162c14cb27",
      "name": "Any",
      "type": "GTPInterfaceProfile",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    }
  },
  "allow-usage-of-static-ip": true,
  "apply-access-policy-on-user-traffic": {
    "enable": false,
    "add-imsi-field-to-log": false
  },
  "imsi-prefix": {
    "enable": true,
    "prefix": "313460000000001"
  },
  "access-point-name": {
    "enable": false
  },
  "selection-mode": {
    "enable": true,
    "mode": 2
  },
  "ms-isdn": {
    "enable": false,
    "ms-isdn": "1"
  },
  "ldap-group": {
    "enable": false,
    "according-to": "MS-ISDN"
  },
  "radio-access-technology": {
    "utran": false,
    "geran": false,
    "wlan": false,
    "gan": false,
    "hspa-evolution": false,
    "eutran": false,
    "virtual": false,
    "nb-iot": false,
    "other-types-range": {
      "enable": false,
      "types": ""
    }
  },
  "trace-management": true,
  "cs-fallback-and-srvcc": false,
  "restoration-and-recovery": false
}
```
