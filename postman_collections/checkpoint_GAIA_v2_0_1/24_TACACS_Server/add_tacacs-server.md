# add tacacs-server

**Collection:** Web API (version 2.0.1) > 24 TACACS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-tacacs-server`

## Description

Add tacacs server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "tacacs7",
  "server": "h1"
}
```

## Example Responses

### Example 1: add tacacs-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c9d1de16-407a-42bc-a28d-3b9d7f933766",
  "name": "tacacs7",
  "type": "tacacs-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1583675379149,
      "iso-8601": "2020-03-08T15:49+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1583675379149,
      "iso-8601": "2020-03-08T15:49+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "groups": [],
  "server-type": "TACACS",
  "server": {
    "name": "h1",
    "uid": "eead9bf5-4640-432c-979b-5d7ae7a8bfb7"
  },
  "priority": 1
}
```
