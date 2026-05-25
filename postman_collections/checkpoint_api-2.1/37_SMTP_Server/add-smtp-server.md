# add-smtp-server

**Collection:** Web API (version 2.1) > 37 SMTP Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-smtp-server`

## Description

Add an SMTP server object to be used when sending emails triggered by SmartTask

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "SMTP1",
  "server": "smtp.example.com",
  "port": "25",
  "encryption": "none"
}
```

## Example Responses

### Example 1: add-smtp-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "84f53517-6b3d-4a23-a959-ad36249de1d7",
  "name": "SMTP1",
  "type": "smtp-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1635951481696,
      "iso-8601": "2021-11-03T16:58+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1635951481696,
      "iso-8601": "2021-11-03T16:58+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "server": "smtp.example.com",
  "port": 25,
  "authentication": false,
  "encryption": "none"
}
```
