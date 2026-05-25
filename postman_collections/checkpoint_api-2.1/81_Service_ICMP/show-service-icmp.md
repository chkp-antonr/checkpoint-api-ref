# show-service-icmp

**Collection:** Web API (version 2.1) > 81 Service ICMP
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-icmp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "info-req"
}
```

## Example Responses

### Example 1: show-service-icmp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "97aeb40f-9aea-11d5-bd16-0090272ccb30",
  "name": "info-req",
  "type": "service-icmp",
  "domain": {
    "domain-type": "data domain",
    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
    "name": "Check Point Data"
  },
  "icmp-type": 15,
  "keep-connections-open-after-policy-installation": false,
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1474568177103,
      "iso-8601": "2016-09-22T21:16+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1474568177103,
      "iso-8601": "2016-09-22T21:16+0300"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": false,
  "comments": "ICMP, info request",
  "color": "orchid",
  "icon": "Services/ICMPService",
  "groups": [
    {
      "uid": "97aeb413-9aea-11d5-bd16-0090272ccb30",
      "name": "icmp-requests",
      "type": "service-group",
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      }
    }
  ]
}
```
