# add-service-tcp

**Collection:** Web API (version 2.0.1) > 68 Service TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_TCP_Service_1",
  "port": 5669,
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 0,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "aggressive-aging": {
    "enable": true,
    "timeout": 360,
    "use-default-timeout": false
  }
}
```

## Example Responses

### Example 1: add-service-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "bee785c5-998b-4a45-80e8-3fa91181aba9",
  "name": "New_TCP_Service_1",
  "type": "service-tcp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479719218212,
      "iso-8601": "2016-11-21T11:06+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479719218212,
      "iso-8601": "2016-11-21T11:06+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/TCPService",
  "groups": [],
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 0,
  "use-default-session-timeout": true,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "aggressive-aging": {
    "enable": true,
    "timeout": 360,
    "use-default-timeout": false,
    "default-timeout": 0
  },
  "port": "5669",
  "match-by-protocol-signature": false
}
```
