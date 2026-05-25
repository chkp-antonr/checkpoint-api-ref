# show-multicast-address-ranges

**Collection:** Web API (version 2.1) > 11 Multicast Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-multicast-address-ranges`

## Description

Displays all Multicast Address Ranges

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full"
}
```

## Example Responses

### Example 1: show-multicast-address-ranges
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "b0f485e1-dc43-4110-bd45-644132f13027",
      "name": "New Multicast Address Range",
      "type": "multicast-address-range",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "locked by current session",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1483966523172,
          "iso-8601": "2017-01-09T14:55+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1483966523172,
          "iso-8601": "2017-01-09T14:55+0200"
        },
        "creator": "aa"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "Objects/ip",
      "groups": [],
      "ipv4-address-first": "224.0.0.1",
      "ipv4-address-last": "224.0.0.4"
    },
    {
      "uid": "fdca71eb-0d30-4750-97d9-457da37a7a99",
      "name": "New Multicast Address Range 2",
      "type": "multicast-address-range",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "locked by current session",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1483966524730,
          "iso-8601": "2017-01-09T14:55+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1483966524730,
          "iso-8601": "2017-01-09T14:55+0200"
        },
        "creator": "aa"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "Objects/ip",
      "groups": [],
      "ipv4-address-first": "224.0.0.19",
      "ipv4-address-last": "224.0.0.19"
    }
  ]
}
```
