# add-service-rpc with group

**Collection:** Web API (version 2.0.1) > 81 Service RPC
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_RPC_Service_2",
  "program-number": 5669,
  "keep-connections-open-after-policy-installation": false,
  "groups": [
    "MY_GROUP"
  ]
}
```

## Example Responses

### Example 1: add-service-rpc with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "66333250-0680-46c3-a894-ebe1fef657f4",
  "name": "New_RPC_Service_2",
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
      "posix": 1453627762831,
      "iso-8601": "2016-01-24T11:29+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1453627762831,
      "iso-8601": "2016-01-24T11:29+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "comments": "",
  "color": "black",
  "icon": "Services/RPCService",
  "groups": [
    {
      "uid": "62bc081a-a09a-4109-a719-b26261780f4c",
      "name": "MY_GROUP",
      "type": "service-group",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    }
  ],
  "keep-connections-open-after-policy-installation": false,
  "program-number": 5669
}
```
