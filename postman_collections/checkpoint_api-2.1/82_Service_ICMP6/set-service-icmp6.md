# set-service-icmp6

**Collection:** Web API (version 2.1) > 82 Service ICMP6
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-service-icmp6`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "icmp1",
  "new-name": "icmp2",
  "icmp-type": 45,
  "icmp-code": 13
}
```

## Example Responses

### Example 1: set-service-icmp6
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d9dcb753-1aa7-4e65-b5ff-b4878f8b3890",
  "name": "icmp4",
  "type": "service-icmp6",
  "domain": {
    "domain-type": "domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "icmp-type": 45,
  "icmp-code": 13,
  "keep-connections-open-after-policy-installation": false,
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1475051901631,
      "iso-8601": "2016-09-28T11:38+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1475051823316,
      "iso-8601": "2016-09-28T11:37+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/ICMPV6Service",
  "groups": []
}
```
