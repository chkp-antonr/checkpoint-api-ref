# set server-certificate name

**Collection:** Web API (version 2.0.1) > 118 Server Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-server-certificate`

## Description

Edit the name of the server certificate.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "MyServerCertificate",
  "new-name": "NewCertificateName"
}
```

## Example Responses

### Example 1: set server-certificate name
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "85944ed6-fa09-40c9-ada9-d980a1dc3f3c",
  "name": "NewCertificateName",
  "type": "server-certificate",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1689251799270,
      "iso-8601": "2023-07-13T15:36+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1689251799270,
      "iso-8601": "2023-07-13T15:36+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "this is a comment",
  "color": "black",
  "icon": "subject_user_certificate",
  "valid-from": "20-Jan-20",
  "valid-to": "17-Jan-30",
  "subject": "O=My Company Ltd,L=Newbury,ST=Berkshire,C=GB"
}
```
