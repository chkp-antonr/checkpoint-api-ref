# show-service-group as ranges

**Collection:** Web API (version 2.1) > 85 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-group`

## Description

Shows a service group with its matched content displayed as ranges of port numbers, and not as Check Point Objects.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "DemoServiceGroup",
  "show-as-ranges": "true"
}
```

## Example Responses

### Example 1: show-service-group as ranges
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "be8c1212-1bb1-43d0-8f19-9641f6bc8714",
  "name": "DemoServiceGroup",
  "type": "service-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1528268364179,
      "iso-8601": "2018-06-06T09:59+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1528268364179,
      "iso-8601": "2018-06-06T09:59+0300"
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
    "tcp": [
      {
        "start": "443",
        "end": "443"
      }
    ],
    "udp": [],
    "others": [],
    "excluded-others": []
  }
}
```
