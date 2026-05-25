# show-service-other

**Collection:** Web API (version 2.1) > 84 Service Other
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-other`

## Request Headers

| Header | Value |
|--------|-------|
| X-chkp-sid |  {{session}} |
| Content-Type |  application/json |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_Service_1"
}
```

## Example Responses

### Example 1: show-service-other
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "25141d14-3e1d-447f-8bc7-a4fe862202be",
  "name": "New_Service_1",
  "type": "service-other",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479721534511,
      "iso-8601": "2016-11-21T11:45+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479721534511,
      "iso-8601": "2016-11-21T11:45+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Services/OtherService",
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
  "ip-protocol": 51,
  "accept-replies": false
}
```
