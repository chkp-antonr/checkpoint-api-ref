# add-service-tcp with protocol

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
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 0,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "aggressive-aging": {
    "enable": true,
    "timeout": 360,
    "use-default-timeout": false
  },
  "protocol": "DNS_TCP",
  "match-by-protocol-signature": true
}
```

## Example Responses

### Example 1: add-service-tcp with protocol
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "49165f0c-9e19-4af1-9e23-f343f873fa53",
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
      "posix": 1479719463450,
      "iso-8601": "2016-11-21T11:11+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479719463450,
      "iso-8601": "2016-11-21T11:11+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Protocols/DNS",
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
  "port": "53",
  "protocol": "DNS_TCP",
  "match-by-protocol-signature": true
}
```
