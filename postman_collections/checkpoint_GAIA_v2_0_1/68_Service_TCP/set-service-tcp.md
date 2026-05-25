# set-service-tcp

**Collection:** Web API (version 2.0.1) > 68 Service TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-service-tcp`

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
  "new-name": "New_TCP_Service_2",
  "color": "green",
  "port": 5656,
  "aggressive-aging": {
    "default-timeout": 3600
  }
}
```

## Example Responses

### Example 1: set-service-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "785a4a8b-8c69-4143-9646-b34ee3b830c5",
  "name": "New_TCP_Service_2",
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
      "posix": 1479719917748,
      "iso-8601": "2016-11-21T11:18+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479719839437,
      "iso-8601": "2016-11-21T11:17+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "light green",
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
    "default-timeout": 3600
  },
  "port": "5656",
  "match-by-protocol-signature": false
}
```
