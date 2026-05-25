# add-group with single member

**Collection:** Web API (version 2.0.1) > 08 Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-group`

## Description

Create a group with single member

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Group 1",
  "members": "New Host 1"
}
```

## Example Responses

### Example 1: add-group with single member
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "20c3aec0-cd48-4223-a118-b0b225a91b78",
  "folder": {
    "uid": "feb54da1-c5e2-4e83-a3ed-d0601ba5ccb9",
    "name": "/Global Objects"
  },
  "domain": {
    "domain-type": "local domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1429440654806,
      "iso-8601": "2015-04-19T13:50+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1429440654806,
      "iso-8601": "2015-04-19T13:50+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Group 2",
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [],
  "members": [
    {
      "folder": {
        "uid": "feb54da1-c5e2-4e83-a3ed-d0601ba5ccb9",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "host",
      "name": "New Host 1",
      "uid": "b1dab55f-4a1e-4776-887f-ed6d7079bc97"
    }
  ]
}
```
