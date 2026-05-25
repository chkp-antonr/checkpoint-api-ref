# set ldap-group

**Collection:** Web API (version 2.0.1) > 142 LDAP Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-ldap-group`

## Description

Edit existing LDAP group.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestLdapGroup",
  "account-unit-branch": "A=B",
  "sub-tree-prefix": "X=Y",
  "group-prefix": "N=TestGroup2",
  "ldap-filter": "N=none"
}
```

## Example Responses

### Example 1: set ldap-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ea4b4c28-76e6-428c-9cc7-b5f553cfa4f0",
  "name": "TestLdapGroup",
  "type": "ldap-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1740386251782,
      "iso-8601": "2025-02-24T10:37+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1740385883268,
      "iso-8601": "2025-02-24T10:31+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/UsersGroup",
  "account-unit": {
    "uid": "ff3c61b0-1f69-4673-a191-485f08c6cf91",
    "name": "TestLdapAccountUnit",
    "type": "CpmiLdapAccountUnit",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/account_unit",
    "color": "black"
  },
  "scope": "only_sub_tree",
  "account-unit-branch": "A=B",
  "sub-tree-prefix": "X=Y",
  "group-prefix": "N=TestGroup2",
  "apply-filter-for-dynamic-group": true,
  "ldap-filter": "N=none"
}
```
