# set-resource-ftp

**Collection:** Web API (version 2.1) > 48 Resource FTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-resource-ftp`

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
  "resource-matching-method": "put"
}
```

## Example Responses

### Example 1: set-resource-ftp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c70617d7-8af4-4237-ab06-15d65e557019",
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
      "posix": 1661254605322,
      "iso-8601": "2022-08-23T14:36+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661254586823,
      "iso-8601": "2022-08-23T14:36+0300"
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
    "uid": "97aeb47d-9aea-11d5-bd16-0090272ccb30",
    "name": "None",
    "type": "CpmiEmptyTrack",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "Track/tracksLog"
  },
  "resource-path": "*",
  "resource-matching-method": "get_and_put",
  "cvp": {
    "enable-cvp": false,
    "cvp-server-is-allowed-to-modify-content": true,
    "reply-order": "return_data_after_content_is_approved"
  }
}
```
