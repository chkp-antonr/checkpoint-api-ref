# set-service-gtp

**Collection:** Web API (version 2.0.1) > 82 Service GTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-service-gtp`

## Description

Modify an existing GTP service

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_gtp_Service_3",
  "new-name": "New_gtp_Service_4",
  "version": "V1"
}
```

## Example Responses

### Example 1: set-service-gtp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ffeef2b8-f902-4d9e-9b3c-dc3a5d1bec5d",
  "name": "New_gtp_Service_4",
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
      "posix": 1587897537632,
      "iso-8601": "2020-04-26T13:38+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1587897475725,
      "iso-8601": "2020-04-26T13:37+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/GTPService",
  "groups": [
    {
      "uid": "5e17676e-205f-4495-a1a3-4fa927fdc395",
      "name": "MY_GROUP",
      "type": "service-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "version": "v1",
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
    "enable": false
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
  }
}
```
