# add-smtp-server with authentication

**Collection:** Web API (version 2.0.1) > 31 SMTP Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-smtp-server`

## Description

Add an SMTP server object with authentication details, to be used when sending emails triggered by SmartTask

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "SMTP2",
  "server": "smtp.example.com",
  "port": "25",
  "authentication": "true",
  "username": "user",
  "password": "password",
  "encryption": "tls"
}
```

## Example Responses

### Example 1: add-smtp-server with authentication
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c45bafae-de18-429d-9d4e-0250bcc2cb78",
  "name": "SMTP2",
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
      "posix": 1635881669778,
      "iso-8601": "2021-11-02T21:34+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1635881669778,
      "iso-8601": "2021-11-02T21:34+0200"
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
  "authentication": true,
  "username": "user",
  "encryption": "tls"
}
```
