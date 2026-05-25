# clone-service-sctp 

**Collection:** Web API (version 2.0.1) > 72 Service SCTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-service-sctp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_SCTP_Service_1",
  "new-name": "New_SCTP_Service_2",
  "color": "green",
  "port": 5656,
  "aggressive-aging": {
    "default-timeout": 3600
  }
}
```

## Example Responses

### Example 1: clone-service-sctp 
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d0385c6d-72dd-4981-b951-4783b7100343",
  "name": "New_SCTP_Service_2",
  "type": "service-sctp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479721010926,
      "iso-8601": "2016-11-21T11:36+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479720948687,
      "iso-8601": "2016-11-21T11:35+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "light green",
  "icon": "Services/SCTPService",
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
  "port": "5656"
}
```
