# add-opsec-application

**Collection:** Web API (version 2.1) > 36 OPSEC Application
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-opsec-application`

## Description

Adds an OPSEC Application

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "MyOpsecApplication",
  "host": "SomeHost",
  "cpmi": {
    "enabled": "true",
    "use-administrator-credentials": "false",
    "administrator-profile": "Super User"
  },
  "lea": {
    "enabled": "false"
  },
  "one-time-password": "SomePassword"
}
```

## Example Responses

### Example 1: add-opsec-application
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1741bb6c-3b19-456c-a635-b96c8456a0e8",
  "name": "MyOpsecApplication",
  "type": "opsec-application",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "host": "SomeHost",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1481003908596,
      "iso-8601": "2016-12-06T07:58+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1481003908596,
      "iso-8601": "2016-12-06T07:58+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "OPSECapplications/OPSEC",
  "cpmi": {
    "use-administrator-credentials": false,
    "administrator-profile": "super user"
  }
}
```
