# clone-service-icmp

**Collection:** Web API (version 2.0.1) > 70 Service ICMP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-service-icmp`

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

### Example 1: clone-service-icmp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "22c8faba-3a24-4e99-ae6f-e798014facc2",
  "name": "icmp3",
  "type": "service-icmp",
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
      "posix": 1475051875083,
      "iso-8601": "2016-09-28T11:37+0300"
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
