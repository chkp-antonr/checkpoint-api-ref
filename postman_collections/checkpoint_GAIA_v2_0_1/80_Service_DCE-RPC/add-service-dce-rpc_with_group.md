# add-service-dce-rpc with group

**Collection:** Web API (version 2.0.1) > 80 Service DCE-RPC
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-dce-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_DCE-RPC_Service_2",
  "interface-uuid": "97aeb460-9aea-11d5-bd16-0090272ccb30",
  "keep-connections-open-after-policy-installation": false,
  "groups": [
    "MY_GROUP"
  ]
}
```

## Example Responses

### Example 1: add-service-dce-rpc with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7d19e3dd-8da5-48a1-b0e0-533fcc0b8dfe",
  "name": "New_DCE-RPC_Service_2",
  "type": "service-dce-rpc",
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
      "posix": 1453627512020,
      "iso-8601": "2016-01-24T11:25+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1453627512020,
      "iso-8601": "2016-01-24T11:25+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "comments": "",
  "color": "black",
  "icon": "Services/DCEService",
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
  "interface-uuid": "97aeb460-9aea-11d5-bd16-0090272ccb30"
}
```
