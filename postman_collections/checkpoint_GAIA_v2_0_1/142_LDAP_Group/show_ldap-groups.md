# show ldap-groups

**Collection:** Web API (version 2.0.1) > 142 LDAP Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-ldap-groups`

## Description

Retrieve all LDAP groups.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5,
  "offset": 0,
  "details-level": "full"
}
```

## Example Responses

### Example 1: show ldap-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
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
          "posix": 1740386251813,
          "iso-8601": "2025-02-24T10:37+0200"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1740385883268,
          "iso-8601": "2025-02-24T10:31+0200"
        },
        "creator": "WEB_API"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "tags": [],
      "read-only": false,
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
        "color": "black",
        "meta-info": {
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1740385545646,
            "iso-8601": "2025-02-24T10:25+0200"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1740385545646,
            "iso-8601": "2025-02-24T10:25+0200"
          },
          "creator": "WEB_API"
        },
        "tags": [],
        "icon": "Objects/account_unit",
        "comments": "",
        "display-name": "",
        "customFields": null
      },
      "scope": "only_sub_tree",
      "account-unit-branch": "A=B",
      "sub-tree-prefix": "X=Y",
      "group-prefix": "N=TestGroup2",
      "apply-filter-for-dynamic-group": true,
      "ldap-filter": "N=none"
    },
    {
      "uid": "690f7327-4afb-4756-90bd-9c55caac1580",
      "name": "TestLdapGroup_Clone",
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
          "posix": 1740386103687,
          "iso-8601": "2025-02-24T10:35+0200"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1740386103687,
          "iso-8601": "2025-02-24T10:35+0200"
        },
        "creator": "WEB_API"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "tags": [],
      "read-only": false,
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
        "color": "black",
        "meta-info": {
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1740385545646,
            "iso-8601": "2025-02-24T10:25+0200"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1740385545646,
            "iso-8601": "2025-02-24T10:25+0200"
          },
          "creator": "WEB_API"
        },
        "tags": [],
        "icon": "Objects/account_unit",
        "comments": "",
        "display-name": "",
        "customFields": null
      },
      "scope": "only_sub_tree",
      "account-unit-branch": "OU=Test",
      "sub-tree-prefix": "CA=AC",
      "group-prefix": "N=TestGroup",
      "apply-filter-for-dynamic-group": true,
      "ldap-filter": "N=AnotherGroup"
    }
  ]
}
```
