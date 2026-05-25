# add radius-group

**Collection:** Web API (version 2.1) > 33 RADIUS Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-radius-group`

## Description

Add radius group

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
    "t4",
    "radgroup"
  ]
}
```

## Example Responses

### Example 1: add radius-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ac07dbd6-29d9-4860-a4b2-a68b99a658d7",
  "name": "group2",
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
      "posix": 1656235257447,
      "iso-8601": "2022-06-26T12:20+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1656235257447,
      "iso-8601": "2022-06-26T12:20+0300"
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
      "uid": "ee5c2c89-d2e9-4b49-a3e5-96ef480be746",
      "name": "radgroup",
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
