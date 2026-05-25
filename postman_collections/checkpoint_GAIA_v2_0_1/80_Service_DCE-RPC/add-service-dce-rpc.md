# add-service-dce-rpc

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
  "name": "New_DCE-RPC_Service_1",
  "interface-uuid": "97aeb460-9aea-11d5-bd16-0090272ccb30",
  "keep-connections-open-after-policy-installation": false
}
```

## Example Responses

### Example 1: add-service-dce-rpc
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b02db15d-c8e9-408c-a789-095b6d76db02",
  "name": "New_DCE-RPC_Service_1",
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
      "posix": 1453627297760,
      "iso-8601": "2016-01-24T11:21+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1453627297760,
      "iso-8601": "2016-01-24T11:21+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "comments": "",
  "color": "black",
  "icon": "Services/DCEService",
  "groups": [],
  "keep-connections-open-after-policy-installation": false,
  "interface-uuid": "97aeb460-9aea-11d5-bd16-0090272ccb30"
}
```
