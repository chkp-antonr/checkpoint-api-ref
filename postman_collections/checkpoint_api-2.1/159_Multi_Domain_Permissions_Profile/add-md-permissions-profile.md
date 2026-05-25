# add-md-permissions-profile

**Collection:** Web API (version 2.1) > 159 Multi Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-md-permissions-profile`

## Description

Add a Multi Domain Permissions Profile with the default permission-level

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "manager profile"
}
```

## Example Responses

### Example 1: add-md-permissions-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "100a2860-1bd3-4402-9dc4-83d52ddd0a84",
  "name": "manager profile",
  "type": "md-permissions-profile",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1640616788167,
      "iso-8601": "2021-12-27T16:53+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1640616788167,
      "iso-8601": "2021-12-27T16:53+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/Role",
  "permission-level": "manager",
  "mds-provisioning": false,
  "manage-all-domains": false,
  "manage-admins": true,
  "manage-sessions": false,
  "management-api-login": true,
  "cme-operations": "disabled",
  "global-vpn-management": false,
  "manage-global-assignments": false,
  "enable-default-profile-for-global-domains": true,
  "default-profile-global-domains": {
    "uid": "f4a23218-5bb9-4880-94bb-9c06b951f195",
    "name": "Read Only All",
    "type": "domain-permissions-profile",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "General/Role",
    "color": "black"
  },
  "view-global-objects-in-domain": true,
  "enable-default-profile-for-local-domains": false
}
```
