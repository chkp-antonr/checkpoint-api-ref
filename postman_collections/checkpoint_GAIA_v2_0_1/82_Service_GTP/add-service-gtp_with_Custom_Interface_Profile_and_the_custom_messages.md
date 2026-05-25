# add-service-gtp with Custom Interface Profile and the custom messages

**Collection:** Web API (version 2.0.1) > 82 Service GTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-gtp`

## Description

Add GTP service with Custom Interface Profile and the custom messages

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_gtp_Service_Custom",
  "version": "V2",
  "interface-profile": {
    "profile": "Custom",
    "custom-message-types": "1-4,7,18,32-35"
  }
}
```

## Example Responses

### Example 1: add-service-gtp with Custom Interface Profile and the custom messages
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "74425232-cadc-49fd-b357-3edbd9b62b14",
  "name": "New_gtp_Service_Custom",
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
      "posix": 1587481750664,
      "iso-8601": "2020-04-21T18:09+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1587481750664,
      "iso-8601": "2020-04-21T18:09+0300"
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
    "uid": "70cf7956-71ab-11ea-bc55-0242ac130003",
    "name": "Custom",
    "type": "GTPInterfaceProfile",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "custom-message-types": "1-4,7,18,32-35",
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
  },
  "trace-management": false,
  "cs-fallback-and-srvcc": false,
  "restoration-and-recovery": false
}
```
