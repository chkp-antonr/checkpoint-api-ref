# clone-resource-uri

**Collection:** Web API (version 2.0.1) > 39 Resource URI
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-resource-uri`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "apiURI"
}
```

## Example Responses

### Example 1: clone-resource-uri
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "24e55329-6b59-4048-b0de-224969e5657a",
  "name": "apiURI_Clone",
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
      "posix": 1661351319496,
      "iso-8601": "2022-08-24T17:28+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661351319496,
      "iso-8601": "2022-08-24T17:28+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "use-this-resource-to": "enforce_uri_capabilities",
  "uri-match-specification-type": "ufp",
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
    "transparent": true,
    "proxy": true,
    "tunneling": false
  },
  "match-ufp": {
    "server": {
      "uid": "2697deef-00f2-4b93-98ad-14289361f326",
      "name": "serverufp",
      "type": "opsec-application",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "OPSECapplications/OPSEC",
      "color": "black"
    },
    "caching-control": "no_caching",
    "ignore-ufp-server-after-failure": false,
    "number-of-failures-before-ignore": 0,
    "timeout-before-reconnecting": 0
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
