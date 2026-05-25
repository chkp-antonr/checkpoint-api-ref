# show-service-tcp

**Collection:** Web API (version 2.0.1) > 68 Service TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-service-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "https"
}
```

## Example Responses

### Example 1: show-service-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30",
  "name": "https",
  "type": "service-tcp",
  "domain": {
    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
    "name": "Check Point Data",
    "domain-type": "data domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479284427934,
      "iso-8601": "2016-11-16T10:20+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1479284427934,
      "iso-8601": "2016-11-16T10:20+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": false,
  "comments": "HTTP protocol over TLS/SSL",
  "color": "red",
  "icon": "Services/TCPService",
  "groups": [
    {
      "uid": "2c21ff3e-cf4a-4ffb-b1c8-eab48b8a2761",
      "name": "Restrict_Common_Protocols_Action",
      "type": "",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 3600,
  "use-default-session-timeout": true,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "aggressive-aging": {
    "enable": true,
    "timeout": 60,
    "use-default-timeout": false,
    "default-timeout": 60
  },
  "port": "443",
  "protocol": "ENC-HTTP",
  "match-by-protocol-signature": false
}
```
