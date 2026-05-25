# set group id

**Collection:** Web API (version 2.1) > 156 Identity Provider Administrator Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-idp-administrator-group`

## Description

set group id

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my global group",
  "group-id": "global-domain-checkpoint"
}
```

## Example Responses

### Example 1: set group id
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "055b2f2f-06a2-48df-922b-47ddfd46f0f8",
  "name": "my global group",
  "type": "idp-administrator-group",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1637846337171,
      "iso-8601": "2021-11-25T15:18+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1637846085472,
      "iso-8601": "2021-11-25T15:14+0200"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/AdministratorGroup",
  "multi-domain-profile": {
    "uid": "6f2d198b-0ca5-480b-88f2-30217da0d635",
    "name": "Global Manager",
    "type": "MDPermissionRole",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "General/Role",
    "color": "black"
  },
  "permissions-profile": [
    {
      "domain": {
        "uid": "18b7fdfa-4fa5-490a-b862-2add6b2ed375",
        "name": "DomA",
        "type": "FolderMirror",
        "domain": {
          "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
          "name": "System Data",
          "domain-type": "mds"
        },
        "icon": "General/globalsNa",
        "color": "black"
      },
      "profile": {
        "uid": "f4a23218-5bb9-4880-94bb-9c06b951f195",
        "name": "Read Only All",
        "type": "PermissionRole",
        "domain": {
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data",
          "domain-type": "data domain"
        },
        "icon": "General/Role",
        "color": "black"
      }
    },
    {
      "domain": {
        "uid": "68efd634-fd04-481b-b62d-99a2a2a6a7d4",
        "name": "All Global Domains",
        "type": "Folder",
        "domain": {
          "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
          "name": "System Data",
          "domain-type": "mds"
        },
        "icon": "Objects/allGlobalDomains",
        "color": "black"
      },
      "profile": {
        "uid": "3c8bf435-6bdc-4dec-aab0-5af53bbf946b",
        "name": "Read Write All",
        "type": "PermissionRole",
        "domain": {
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data",
          "domain-type": "data domain"
        },
        "icon": "General/Role",
        "color": "black"
      }
    }
  ],
  "group-id": "global-domain-checkpoint"
}
```
