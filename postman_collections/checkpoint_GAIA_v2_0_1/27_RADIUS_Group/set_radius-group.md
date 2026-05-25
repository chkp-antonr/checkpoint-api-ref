# set radius-group

**Collection:** Web API (version 2.0.1) > 27 RADIUS Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-radius-group`

## Description

Set radius group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "radgroup",
  "members": [
    "t4"
  ]
}
```

## Example Responses

### Example 1: set radius-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ee5c2c89-d2e9-4b49-a3e5-96ef480be746",
  "name": "radgroup",
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
      "posix": 1656238796470,
      "iso-8601": "2022-06-26T13:19+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1655388732862,
      "iso-8601": "2022-06-16T17:12+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [
    {
      "uid": "cc17f634-00a9-4b9d-8c0b-2a3c700a3413",
      "name": "myspecialgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "51c85bec-4013-48eb-b5f8-ac25b2244002",
      "name": "testgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    }
  ],
  "members": [
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
    }
  ]
}
```
