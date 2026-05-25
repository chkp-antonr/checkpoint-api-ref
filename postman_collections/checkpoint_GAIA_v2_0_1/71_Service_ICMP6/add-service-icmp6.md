# add-service-icmp6

**Collection:** Web API (version 2.0.1) > 71 Service ICMP6
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-icmp6`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Icmp1",
  "icmp-type": 5,
  "icmp-code": 7
}
```

## Example Responses

### Example 1: add-service-icmp6
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d9dcb753-1aa7-4e65-b5ff-b4878f8b3890",
  "name": "Icmp2",
  "type": "service-icmp6",
  "domain": {
    "domain-type": "domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "icmp-type": 5,
  "icmp-code": 7,
  "keep-connections-open-after-policy-installation": false,
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1475051823316,
      "iso-8601": "2016-09-28T11:37+0300"
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
