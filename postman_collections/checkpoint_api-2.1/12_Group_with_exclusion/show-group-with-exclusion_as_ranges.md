# show-group-with-exclusion as ranges

**Collection:** Web API (version 2.1) > 12 Group with exclusion
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-group-with-exclusion`

## Description

Shows a group with exclusion with its matched content displayed as ranges of IP addresses, and not as Check Point Objects.The ranges of IP addresses of the 'except' part is subtracted from the ranges of IP addresses of the 'include' part.In this example, the 'include' part contains the network 10.10.10.0/24 and the 'except' part contains the network 10.10.10.128/25.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "DemoGroupWithExclusion",
  "show-as-ranges": "true"
}
```

## Example Responses

### Example 1: show-group-with-exclusion as ranges
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "dce451da-c9c7-46a9-bdb5-8fc953a6f172",
  "name": "DemoGroupWithExclusion",
  "type": "group-with-exclusion",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1528268215283,
      "iso-8601": "2018-06-06T09:56+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1528268215283,
      "iso-8601": "2018-06-06T09:56+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "ranges": {
    "ipv4": [
      {
        "start": "10.10.10.0",
        "end": "10.10.10.127"
      },
      {
        "start": "10.10.14.1",
        "end": "10.10.14.1"
      }
    ],
    "ipv6": [],
    "others": [],
    "excluded-others": []
  }
}
```
