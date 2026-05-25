# add-service-gtp with Access Point Name

**Collection:** Web API (version 2.1) > 93 Service GTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-gtp`

## Description

Add GTP service with match by Access Point Name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_gtp_Service_2",
  "version": "V2",
  "access-point-name": {
    "enable": true,
    "apn": "APN_Object1"
  }
}
```

## Example Responses

### Example 1: add-service-gtp with Access Point Name
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "725acf3e-324a-4167-9d4b-684d62b0d712",
  "name": "New_gtp_Service_2",
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
      "posix": 1587897421315,
      "iso-8601": "2020-04-26T13:37+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1587897421315,
      "iso-8601": "2020-04-26T13:37+0300"
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
    "enable": false,
    "prefix": "1"
  },
  "access-point-name": {
    "enable": true,
    "apn": {
      "uid": "bce4c57b-07d8-49a2-8f01-b6b46124c275",
      "name": "APN_Object1",
      "type": "CpmiGprsApn",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  },
  "selection-mode": {
    "enable": false,
    "mode": 0
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
  "trace-management": false,
  "cs-fallback-and-srvcc": false,
  "restoration-and-recovery": false
}
```
