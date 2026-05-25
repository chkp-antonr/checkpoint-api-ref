# add-service-tcp with group

**Collection:** Web API (version 2.1) > 79 Service TCP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-tcp`

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
  },
  "groups": [
    "MY_GROUP"
  ]
}
```

## Example Responses

### Example 1: add-service-tcp with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "59c19723-ce20-45f0-a4af-bcd2375c92a5",
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
      "posix": 1479719390225,
      "iso-8601": "2016-11-21T11:09+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479719390225,
      "iso-8601": "2016-11-21T11:09+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/TCPService",
  "groups": [
    {
      "uid": "61a9de0a-f624-4c9b-b178-180a0a1c4c0b",
      "name": "MY_GROUP",
      "type": "service-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
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
