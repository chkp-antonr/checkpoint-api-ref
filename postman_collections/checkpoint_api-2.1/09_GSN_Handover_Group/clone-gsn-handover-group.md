# clone-gsn-handover-group

**Collection:** Web API (version 2.1) > 09 GSN Handover Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-gsn-handover-group`

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
  "enforce-gtp": false,
  "members": {
    "add": "CP_default_Office_Mode_addresses_pool"
  }
}
```

## Example Responses

### Example 1: clone-gsn-handover-group
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
    },
    {
      "uid": "0fbffeda-b4cb-429d-a6c0-f54f1132e63c",
      "name": "CP_default_Office_Mode_addresses_pool",
      "type": "network",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "subnet4": "172.16.10.0",
      "subnet-mask": "255.255.255.0",
      "mask-length4": 24
    }
  ],
  "enforce-gtp": false,
  "gtp-rate": 2048
}
```
