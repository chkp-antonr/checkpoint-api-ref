# add-gsn-handover-group

**Collection:** Web API (version 2.0.1) > 09 GSN Handover Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-gsn-handover-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gsnhandovergroup",
  "enforce-gtp": true,
  "gtp-rate": 2048,
  "members": [
    "All_Internet"
  ]
}
```

## Example Responses

### Example 1: add-gsn-handover-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f140a9d1-4167-456a-931d-abdaa4c8aa7e",
  "name": "gsnhandovergroup",
  "type": "gsn-handover-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [],
  "members": [
    {
      "uid": "29438958-5569-49b7-a270-dfff5be51c3a",
      "name": "All_Internet",
      "type": "address-range",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address-first": "0.0.0.0",
      "ipv4-address-last": "255.255.255.255"
    }
  ],
  "enforce-gtp": true,
  "gtp-rate": 2048
}
```
