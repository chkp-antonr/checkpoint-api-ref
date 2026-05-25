# clone radius-group

**Collection:** Web API (version 2.0.1) > 27 RADIUS Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-radius-group`

## Description

Clone radius group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "group1"
}
```

## Example Responses

### Example 1: clone radius-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7df5d825-884f-441b-ad0e-db58d85f70a6",
  "name": "newgroup_Clone",
  "type": "radius-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1656241511164,
      "iso-8601": "2022-06-26T14:05+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1656241511164,
      "iso-8601": "2022-06-26T14:05+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [],
  "members": [
    {
      "uid": "ec5a8725-cde2-4107-863d-aa2e7a2d7ed3",
      "name": "test",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "f99ccf83-dbf9-40b9-9142-cda575b9e956",
      "name": "t4",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "0bdcf1cf-d8e6-48c4-be5c-ee4270ab35cc",
      "name": "uidradiusgroup",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    }
  ]
}
```
