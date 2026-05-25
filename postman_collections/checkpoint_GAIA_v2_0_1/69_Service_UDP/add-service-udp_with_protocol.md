# add-service-udp with protocol

**Collection:** Web API (version 2.0.1) > 69 Service UDP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-udp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_UDP_Service_1",
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 0,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "aggressive-aging": {
    "enable": true,
    "timeout": 360,
    "use-default-timeout": false
  },
  "accept-replies": false,
  "protocol": "tftp",
  "match-by-protocol-signature": true
}
```

## Example Responses

### Example 1: add-service-udp with protocol
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ae4e3c2e-8368-4b98-9846-6391770a81aa",
  "name": "New_UDP_Service_1",
  "type": "service-udp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479720519849,
      "iso-8601": "2016-11-21T11:28+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479720519849,
      "iso-8601": "2016-11-21T11:28+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Protocols/FTP",
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
  "port": "69",
  "protocol": "TFTP",
  "match-by-protocol-signature": true,
  "accept-replies": false
}
```
