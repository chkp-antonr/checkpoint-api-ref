# add ldap-group

**Collection:** Web API (version 2.1) > 153 LDAP Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-ldap-group`

## Description

Create new LDAP group.

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
  "account-unit": "TestLdapAccountUnit",
  "scope": "only_sub_tree",
  "account-unit-branch": "OU=Test",
  "sub-tree-prefix": "CA=AC",
  "group-prefix": "N=TestGroup",
  "apply-filter-for-dynamic-group": true,
  "ldap-filter": "N=AnotherGroup"
}
```

## Example Responses

### Example 1: add ldap-group
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
      "posix": 1740385883179,
      "iso-8601": "2025-02-24T10:31+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1740385883179,
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
  "account-unit-branch": "OU=Test",
  "sub-tree-prefix": "CA=AC",
  "group-prefix": "N=TestGroup",
  "apply-filter-for-dynamic-group": true,
  "ldap-filter": "N=AnotherGroup"
}
```
