# add-host with group

**Collection:** Web API (version 2.1) > 05 Host
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-host`

## Description

Adds simple host with group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Host 2",
  "ip-address": "192.0.2.2",
  "groups": [
    "New Group 1",
    "New Group 2"
  ]
}
```

## Example Responses

### Example 1: add-host with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "00ff73b3-c1d5-46c2-97a1-0540c82094c2",
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
      "posix": 1435470679142,
      "iso-8601": "2015-06-28T08:51+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1435470679142,
      "iso-8601": "2015-06-28T08:51+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Host 2",
  "comments": "",
  "color": "black",
  "icon": "Objects/host",
  "groups": [
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
      "type": "group",
      "name": "New Group 1",
      "uid": "d20710f1-831c-49dd-a009-aa9e569f643a"
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
      "type": "group",
      "name": "New Group 2",
      "uid": "6e3e3f33-fc23-433d-ac90-d72196f9ffcf"
    }
  ],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "192.0.2.1"
}
```
