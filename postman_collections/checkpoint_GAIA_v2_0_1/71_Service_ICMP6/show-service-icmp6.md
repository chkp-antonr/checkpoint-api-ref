# show-service-icmp6

**Collection:** Web API (version 2.0.1) > 71 Service ICMP6
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-service-icmp6`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "echo-reply6"
}
```

## Example Responses

### Example 1: show-service-icmp6
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ac85a522-916a-4ce0-8411-32d1d0016348",
  "name": "echo-reply6",
  "type": "service-icmp6",
  "domain": {
    "domain-type": "data domain",
    "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
    "name": "Check Point Data"
  },
  "icmp-type": 129,
  "keep-connections-open-after-policy-installation": false,
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1474568177091,
      "iso-8601": "2016-09-22T21:16+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1474568177091,
      "iso-8601": "2016-09-22T21:16+0300"
    },
    "creator": "System"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "blue",
  "icon": "Services/ICMPV6Service",
  "groups": []
}
```
