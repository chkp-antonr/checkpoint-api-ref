# add-multicast-address-range-single-ip

**Collection:** Web API (version 2.0.1) > 11 Multicast Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-multicast-address-range`

## Description

Adds a new Multicast Address Range using a single IP Address

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Multicast Address Range 2",
  "ip-address": "224.0.0.19"
}
```

## Example Responses

### Example 1: add-multicast-address-range-single-ip
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4876c0f0-95a8-43b7-8749-e0a3ade78ae6",
  "name": "New Multicast Address Range 2",
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
      "posix": 1483966323491,
      "iso-8601": "2017-01-09T14:52+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1483966323491,
      "iso-8601": "2017-01-09T14:52+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/ip",
  "groups": [],
  "ipv4-address-first": "224.0.0.19",
  "ipv4-address-last": "224.0.0.19"
}
```
