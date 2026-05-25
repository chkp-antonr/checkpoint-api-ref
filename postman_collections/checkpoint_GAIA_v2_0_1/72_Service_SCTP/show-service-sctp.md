# show-service-sctp

**Collection:** Web API (version 2.0.1) > 72 Service SCTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-service-sctp`

## Request Headers

| Header | Value |
|--------|-------|
| X-chkp-sid |  {{session}} |
| Content-Type |  application/json |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_SCTP_Service_1"
}
```

## Example Responses

### Example 1: show-service-sctp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f04b754f-f190-4c79-afb1-d72821478d3a",
  "name": "New_SCTP_Service_1",
  "type": "service-sctp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479721214735,
      "iso-8601": "2016-11-21T11:40+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479721214735,
      "iso-8601": "2016-11-21T11:40+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
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
    "default-timeout": 0
  },
  "port": "5669"
}
```
