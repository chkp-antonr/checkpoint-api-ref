# show tacacs-server

**Collection:** Web API (version 2.0.1) > 24 TACACS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-tacacs-server`

## Description

Show tacacs server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "t1"
}
```

## Example Responses

### Example 1: show tacacs-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5ea8956b-dca3-4a0c-b75a-1644bd41ab2b",
  "name": "t1",
  "type": "tacacs",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by other session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1581497843922,
      "iso-8601": "2020-02-12T10:57+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1581497843922,
      "iso-8601": "2020-02-12T10:57+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "groups": [],
  "server-type": "tacacs",
  "server": "d700e8d5-d010-4f37-ab14-f78f5a26426c",
  "priority": 1
}
```
