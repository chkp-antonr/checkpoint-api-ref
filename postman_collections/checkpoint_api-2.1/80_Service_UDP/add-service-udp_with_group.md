# add-service-udp with group

**Collection:** Web API (version 2.1) > 80 Service UDP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-udp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_UDP_Service_2",
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
  "accept-replies": false,
  "groups": [
    "MY_GROUP"
  ]
}
```

## Example Responses

### Example 1: add-service-udp with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d740af8d-e6e1-48e3-94a5-1d10462e6b4a",
  "name": "New_UDP_Service_2",
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
      "posix": 1479720440924,
      "iso-8601": "2016-11-21T11:27+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479720440924,
      "iso-8601": "2016-11-21T11:27+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/UDPService",
  "groups": [
    {
      "uid": "a4c6342f-7962-49d9-aa4e-12d6c8aa5a06",
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
  "match-by-protocol-signature": false,
  "accept-replies": false
}
```
