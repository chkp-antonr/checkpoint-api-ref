# add-service-icmp

**Collection:** Web API (version 2.1) > 81 Service ICMP
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-icmp`

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

### Example 1: add-service-icmp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "22c8faba-3a24-4e99-ae6f-e798014facc2",
  "name": "Icmp1",
  "type": "service-icmp",
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
      "posix": 1475051751286,
      "iso-8601": "2016-09-28T11:35+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1475051751286,
      "iso-8601": "2016-09-28T11:35+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/ICMPService",
  "groups": []
}
```
