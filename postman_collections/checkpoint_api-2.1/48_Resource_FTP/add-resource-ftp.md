# add-resource-ftp

**Collection:** Web API (version 2.1) > 48 Resource FTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-resource-ftp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newFtpResource",
  "resource-matching-method": "get_and_put",
  "exception-track": "exception log",
  "resources-path": "path"
}
```

## Example Responses

### Example 1: add-resource-ftp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ad837f52-1973-4f85-a48c-b3e6d7f88059",
  "name": "newFtpResource",
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
      "posix": 1661240575558,
      "iso-8601": "2022-08-23T10:42+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661240575558,
      "iso-8601": "2022-08-23T10:42+0300"
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
  "resource-path": "path",
  "resource-matching-method": "get_and_put",
  "cvp": {
    "enable-cvp": false,
    "cvp-server-is-allowed-to-modify-content": true,
    "reply-order": "return_data_after_content_is_approved"
  }
}
```
