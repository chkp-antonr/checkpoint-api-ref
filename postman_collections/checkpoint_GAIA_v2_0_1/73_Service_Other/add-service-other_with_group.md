# add-service-other with group  

**Collection:** Web API (version 2.0.1) > 73 Service Other
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-other`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_Service_2",
  "keep-connections-open-after-policy-installation": false,
  "session-timeout": 0,
  "match-for-any": true,
  "sync-connections-on-cluster": true,
  "ip-protocol": 51,
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

### Example 1: add-service-other with group  
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6ed7d4c0-be35-469b-a923-d29bb1add889",
  "name": "New_Service_2",
  "type": "service-other",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1479721442140,
      "iso-8601": "2016-11-21T11:44+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1479721442140,
      "iso-8601": "2016-11-21T11:44+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/OtherService",
  "groups": [
    {
      "uid": "316a8f04-bf5d-4067-8d91-6f3c42816157",
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
  "ip-protocol": 51,
  "accept-replies": false
}
```
