# add group with domain super user profile

**Collection:** Web API (version 2.1) > 156 Identity Provider Administrator Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-idp-administrator-group`

## Description

add group with domain super user profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my super group",
  "group-id": "it-team",
  "multi-domain-profile": "domain super user"
}
```

## Example Responses

### Example 1: add group with domain super user profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "799fba94-d915-46d0-82a6-6e6bf369e87c",
  "name": "my super group",
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
      "posix": 1637845907740,
      "iso-8601": "2021-11-25T15:11+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1637845907740,
      "iso-8601": "2021-11-25T15:11+0200"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/AdministratorGroup",
  "multi-domain-profile": {
    "uid": "fc548fad-48ab-4bbe-b693-00105d536006",
    "name": "Domain Super User",
    "type": "MDPermissionRole",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "General/Role",
    "color": "black"
  },
  "group-id": "it-team"
}
```
