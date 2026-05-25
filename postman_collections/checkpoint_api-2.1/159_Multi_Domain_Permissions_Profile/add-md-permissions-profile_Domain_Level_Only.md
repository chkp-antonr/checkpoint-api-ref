# add-md-permissions-profile (Domain Level Only)

**Collection:** Web API (version 2.1) > 159 Multi Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-md-permissions-profile`

## Description

Add a Domain Level Only profile with a default profile for all local domains

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain level only profile",
  "permission-level": "domain level only",
  "enable-default-profile-for-local-domains": "true",
  "default-profile-local-domains": "read only all"
}
```

## Example Responses

### Example 1: add-md-permissions-profile (Domain Level Only)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2587fcea-9584-4f01-8412-2ae90afbf2bb",
  "name": "domain level only profile",
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
      "posix": 1640685250021,
      "iso-8601": "2021-12-28T11:54+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1640685250021,
      "iso-8601": "2021-12-28T11:54+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/Role",
  "permission-level": "domain level only",
  "mds-provisioning": false,
  "manage-all-domains": false,
  "manage-admins": false,
  "manage-sessions": false,
  "management-api-login": true,
  "cme-operations": "disabled",
  "global-vpn-management": false,
  "manage-global-assignments": false,
  "enable-default-profile-for-global-domains": false,
  "view-global-objects-in-domain": true,
  "enable-default-profile-for-local-domains": true,
  "default-profile-local-domains": {
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
  }
}
```
