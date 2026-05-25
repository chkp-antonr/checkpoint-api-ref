# show-groups as ranges

**Collection:** Web API (version 2.1) > 08 Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-groups`

## Description

Shows the first 50 groups with each group's matched content displayed as ranges of IP addresses, and not as Check Point Objects.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "full",
  "show-as-ranges": "true"
}
```

## Example Responses

### Example 1: show-groups as ranges
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "f4f16175-00ba-4478-9439-a2181d96c446",
      "name": "Demo_Group",
      "type": "group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "locked by current session",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1528267848679,
          "iso-8601": "2018-06-06T09:50+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1528267722225,
          "iso-8601": "2018-06-06T09:48+0300"
        },
        "creator": "aa"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "General/group",
      "groups": [],
      "ranges": {
        "ipv4": [
          {
            "start": "10.10.10.0",
            "end": "10.10.10.255"
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
  ]
}
```
