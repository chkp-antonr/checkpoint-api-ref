# add-multicast-address-range-ip-range

**Collection:** Web API (version 2.1) > 11 Multicast Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-multicast-address-range`

## Description

Adds a new Multicast Address Range using a range of IP Addresses

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Multicast Address Range",
  "ip-address-first": "224.0.0.1",
  "ip-address-last": "224.0.0.4"
}
```

## Example Responses

### Example 1: add-multicast-address-range-ip-range
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "faff3fdf-01b9-4c58-97dc-176c409b5bc1",
  "name": "New Multicast Address Range",
  "type": "multicast-address-range",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1483966213026,
      "iso-8601": "2017-01-09T14:50+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1483966213026,
      "iso-8601": "2017-01-09T14:50+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/ip",
  "groups": [],
  "ipv4-address-first": "224.0.0.1",
  "ipv4-address-last": "224.0.0.4"
}
```
