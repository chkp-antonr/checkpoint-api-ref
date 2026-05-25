# show-resource-uri

**Collection:** Web API (version 2.1) > 46 Resource URI
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-resource-uri`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newUriResource"
}
```

## Example Responses

### Example 1: show-resource-uri
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6781f656-575f-46f0-8be2-0bcb399d12b2",
  "name": "newUriResource",
  "type": "resource-uri",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1661243987400,
      "iso-8601": "2022-08-23T11:39+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661243987400,
      "iso-8601": "2022-08-23T11:39+0300"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "use-this-resource-to": "optimize_url_logging",
  "uri-match-specification-type": "wildcards",
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
  "connection-methods": {
    "transparent": false,
    "proxy": true,
    "tunneling": true
  },
  "match-wildcards": {
    "host": "hostName",
    "path": "pathName",
    "query": "*",
    "schemes": {
      "http": false,
      "ftp": false,
      "gopher": false,
      "mailto": false,
      "news": false,
      "wais": false,
      "other": "*"
    },
    "methods": {
      "get": false,
      "post": false,
      "head": false,
      "put": false,
      "other": "*"
    }
  },
  "action": {
    "strip-script-tags": false,
    "strip-applet-tags": false,
    "strip-activex-tags": false,
    "strip-ftp-links": false,
    "strip-port-strings": false
  },
  "cvp": {
    "enable-cvp": false,
    "cvp-server-is-allowed-to-modify-content": true,
    "reply-order": "return_data_after_content_is_approved",
    "send-http-headers-to-cvp": false,
    "send-http-request-to-cvp": false,
    "send-only-unsafe-file-types": true
  },
  "soap": {
    "inspection": "allow_all_soap_requests",
    "file-id": "scheme1",
    "track-connections": "none"
  }
}
```
