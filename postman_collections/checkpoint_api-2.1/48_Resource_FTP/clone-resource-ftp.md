# clone-resource-ftp

**Collection:** Web API (version 2.1) > 48 Resource FTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-resource-ftp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myftp"
}
```

## Example Responses

### Example 1: clone-resource-ftp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d0839fc8-5d38-4912-a403-098ab3ac870c",
  "name": "myftp_Clone",
  "type": "resource-ftp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1661350804084,
      "iso-8601": "2022-08-24T17:20+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661350804084,
      "iso-8601": "2022-08-24T17:20+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "exception-track": {
    "uid": "97aeb48d-9aea-11d5-bd16-0090272ccb30",
    "name": "Exception Log",
    "type": "CpmiLog",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "Track/tracksLog",
    "color": "blue"
  },
  "resource-path": "pathy",
  "resource-matching-method": "get",
  "cvp": {
    "enable-cvp": true,
    "server": {
      "uid": "fd3ef20e-ac64-476f-91c8-1b9c579a3f84",
      "name": "opsec",
      "type": "opsec-application",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "OPSECapplications/OPSEC",
      "color": "black"
    },
    "cvp-server-is-allowed-to-modify-content": true,
    "reply-order": "return_data_after_content_is_approved"
  }
}
```
