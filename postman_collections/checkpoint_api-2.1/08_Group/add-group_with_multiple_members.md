# add-group with multiple members

**Collection:** Web API (version 2.1) > 08 Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-group`

## Description

Create a group with multiple members

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Group 4",
  "members": [
    "New Host 1",
    "My Test Host 3"
  ]
}
```

## Example Responses

### Example 1: add-group with multiple members
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3417b105-b1bb-4088-8106-2fff89ea47b1",
  "folder": {
    "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
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
      "posix": 1435472184133,
      "iso-8601": "2015-06-28T09:16+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1435472184133,
      "iso-8601": "2015-06-28T09:16+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Group 4",
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [],
  "members": [
    {
      "folder": {
        "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "host",
      "name": "My Test Host 3",
      "uid": "56e38c35-af6b-4310-9c8c-4f128e61ef1e"
    },
    {
      "folder": {
        "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "host",
      "name": "New Host 1",
      "uid": "280ff2f7-2ce2-42ac-a29f-cad26a4d6de5"
    }
  ]
}
```
