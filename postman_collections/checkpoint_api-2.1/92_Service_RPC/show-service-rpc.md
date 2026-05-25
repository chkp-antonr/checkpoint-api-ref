# show-service-rpc

**Collection:** Web API (version 2.1) > 92 Service RPC
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "nisplus"
}
```

## Example Responses

### Example 1: show-service-rpc
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "97aeb3c6-9aea-11d5-bd16-0090272ccb30",
  "name": "nisplus",
  "type": "service-rpc",
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
      "posix": 1453368095037,
      "iso-8601": "2016-01-21T11:21+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1453368095037,
      "iso-8601": "2016-01-21T11:21+0200"
    },
    "creator": "System"
  },
  "tags": [],
  "comments": "NIS+ later version provides additional security and other facilities",
  "color": "navy blue",
  "icon": "Services/RPCService",
  "groups": [],
  "keep-connections-open-after-policy-installation": false,
  "program-number": 100300
}
```
