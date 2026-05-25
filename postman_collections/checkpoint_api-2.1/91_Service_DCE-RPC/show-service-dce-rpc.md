# show-service-dce-rpc

**Collection:** Web API (version 2.1) > 91 Service DCE-RPC
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-dce-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "HP-OpCdistm"
}
```

## Example Responses

### Example 1: show-service-dce-rpc
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "97aeb460-9aea-11d5-bd16-0090272ccb30",
  "name": "HP-OpCdistm",
  "type": "service-dce-rpc",
  "domain": {
    "domain-type": "data domain",
    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
    "name": "Check Point Data"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1453368096819,
      "iso-8601": "2016-01-21T11:21+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1453368096819,
      "iso-8601": "2016-01-21T11:21+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "comments": "HP-OV OpC Distribution Manager",
  "color": "blue",
  "icon": "Services/DCEService",
  "groups": [],
  "keep-connections-open-after-policy-installation": false,
  "interface-uuid": "5df3dc6f-a568-0000-020f-887805000000"
}
```
