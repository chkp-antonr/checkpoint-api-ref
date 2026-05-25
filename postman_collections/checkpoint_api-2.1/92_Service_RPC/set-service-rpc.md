# set-service-rpc

**Collection:** Web API (version 2.1) > 92 Service RPC
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-service-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_RPC_Service_1",
  "new-name": "New_RPC_Service_5",
  "color": "green",
  "program-number": 5656
}
```

## Example Responses

### Example 1: set-service-rpc
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "55023213-9bdd-4f7c-9a41-342938de74ba",
  "name": "New_RPC_Service_5",
  "type": "service-rpc",
  "domain": {
    "domain-type": "domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1453627813327,
      "iso-8601": "2016-01-24T11:30+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1453627724762,
      "iso-8601": "2016-01-24T11:28+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "comments": "",
  "color": "green",
  "icon": "Services/RPCService",
  "groups": [],
  "keep-connections-open-after-policy-installation": false,
  "program-number": 5656
}
```
