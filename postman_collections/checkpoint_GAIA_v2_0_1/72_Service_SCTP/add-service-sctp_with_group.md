# add-service-sctp with group 

**Collection:** Web API (version 2.0.1) > 72 Service SCTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-sctp`

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

### Example 1: add-service-sctp with group 
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8a1da428-db25-4ae8-8f7c-88a0d5526da8",
  "name": "New_SCTP_Service_1",
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
      "posix": 1479721140635,
      "iso-8601": "2016-11-21T11:39+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479721140635,
      "iso-8601": "2016-11-21T11:39+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/SCTPService",
  "groups": [
    {
      "uid": "a16b7bd1-9209-40d2-982e-b782ed3e60f5",
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
  "port": "5669"
}
```
