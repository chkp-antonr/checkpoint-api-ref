# clone tacacs-server

**Collection:** Web API (version 2.1) > 30 TACACS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-tacacs-server`

## Description

Clone tacacs server name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "tacacs server",
  "priority": "5",
  "encryption": "true",
  "secret-key": "**secret**",
  "server": "d700e8d5-d010-4f37-ab14-f78f5a26426c",
  "server-type": "TACACS"
}
```

## Example Responses

### Example 1: clone tacacs-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ae2025ae-3f63-44de-92c7-d5b423f93a57",
  "name": "tacacs server",
  "type": "tacacs",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1582719187182,
      "iso-8601": "2020-02-26T14:13+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1582719187182,
      "iso-8601": "2020-02-26T14:13+0200"
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
  "priority": 5
}
```
