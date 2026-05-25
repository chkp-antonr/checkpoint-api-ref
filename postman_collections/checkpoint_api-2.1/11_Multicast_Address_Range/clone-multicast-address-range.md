# clone-multicast-address-range

**Collection:** Web API (version 2.1) > 11 Multicast Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-multicast-address-range`

## Description

Clones an existing Multicast Address Range

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
  "ip-address-first": "224.0.0.7",
  "ip-address-last": "224.0.0.10"
}
```

## Example Responses

### Example 1: clone-multicast-address-range
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "77c85c47-0fff-4c36-afab-6c04fc118bc7",
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
      "posix": 1483966436311,
      "iso-8601": "2017-01-09T14:53+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1483966435089,
      "iso-8601": "2017-01-09T14:53+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/ip",
  "groups": [],
  "ipv4-address-first": "224.0.0.7",
  "ipv4-address-last": "224.0.0.10"
}
```
