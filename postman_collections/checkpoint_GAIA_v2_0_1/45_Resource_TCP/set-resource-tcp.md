# set-resource-tcp

**Collection:** Web API (version 2.0.1) > 45 Resource TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-resource-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newTcpResource",
  "new-name": "tcpResource",
  "ufp-settings": {
    "caching-control": "ufp_server",
    "ignore-ufp-server-after-failure": false,
    "number-of-failures-before-ignore": 0
  },
  "cvp-settings": {
    "server": "cvpServer"
  }
}
```

## Example Responses

### Example 1: set-resource-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b65433d5-409b-4dda-8fcd-b87d82e9f0cb",
  "name": "tcpResource",
  "type": "resource-tcp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1750080492472,
      "iso-8601": "2025-06-16T16:28+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1750079443220,
      "iso-8601": "2025-06-16T16:10+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "resource-type": "ufp",
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
  "cvp-settings": {
    "server": {
      "uid": "39ab54cf-41c5-495d-9815-96e637ee9c29",
      "name": "cvpServer",
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
  },
  "ufp-settings": {
    "server": {
      "uid": "cb52be7d-4d7b-400b-aa6a-816c9a3ffd5f",
      "name": "ufpServer",
      "type": "opsec-application",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "OPSECapplications/OPSEC",
      "color": "black"
    },
    "caching-control": "ufp_server",
    "ignore-ufp-server-after-failure": false,
    "number-of-failures-before-ignore": 0,
    "timeout-before-reconnecting": 0
  }
}
```
