# show all idp-to-domain-assignments objects

**Collection:** Web API (version 2.1) > 161 Identity Provider To Domain Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-idp-to-domain-assignments`

## Description

show all idp-to-domain-assignments objects

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

### Example 1: show all idp-to-domain-assignments objects
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": -1,
  "objects": [
    {
      "uid": "fe866287-248a-4fb3-9e5e-bb0e1ac90788",
      "type": "idp-to-domain-assignment",
      "domain": {
        "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
        "name": "System Data",
        "domain-type": "mds"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1642077724898,
          "iso-8601": "2022-01-13T14:42+0200"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1641462834333,
          "iso-8601": "2022-01-06T11:53+0200"
        },
        "creator": "System"
      },
      "tags": [],
      "read-only": false,
      "identity-provider-set": false,
      "using-default": true,
      "assigned-domain": {
        "uid": "e6e6cc24-9881-4869-975c-7b3ac8d4347d",
        "name": "BSMS",
        "type": "domain",
        "domain": {
          "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
          "name": "System Data",
          "domain-type": "mds"
        },
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1641463212554,
            "iso-8601": "2022-01-06T12:00+0200"
          },
          "last-modifier": "System",
          "creation-time": {
            "posix": 1641462830597,
            "iso-8601": "2022-01-06T11:53+0200"
          },
          "creator": "aa"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "Objects/domain",
        "domain-type": "domain",
        "servers": [
          {
            "name": "BSMS_Server",
            "type": "management server",
            "ipv4-address": "172.28.2.121",
            "multi-domain-server": "Firewall-ivory-main-take-263",
            "active": true
          }
        ],
        "global-domain-assignments": []
      }
    },
    {
      "uid": "2feed858-373b-4618-ae03-84e1a08bad72",
      "type": "idp-to-domain-assignment",
      "domain": {
        "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
        "name": "System Data",
        "domain-type": "mds"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1642078321824,
          "iso-8601": "2022-01-13T14:52+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1641229065206,
          "iso-8601": "2022-01-03T18:57+0200"
        },
        "creator": "System"
      },
      "tags": [],
      "read-only": false,
      "identity-provider-set": false,
      "using-default": true,
      "assigned-domain": {
        "uid": "8ecf2426-268d-44c6-95c6-85289d34318f",
        "name": "SMS",
        "type": "domain",
        "domain": {
          "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
          "name": "System Data",
          "domain-type": "mds"
        },
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1641229402073,
            "iso-8601": "2022-01-03T19:03+0200"
          },
          "last-modifier": "arig@checkpoint.com",
          "creation-time": {
            "posix": 1641229063850,
            "iso-8601": "2022-01-03T18:57+0200"
          },
          "creator": "Remote CPM Server"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "Objects/domain",
        "domain-type": "domain",
        "servers": [
          {
            "name": "SMS_Server",
            "type": "management server",
            "ipv4-address": "172.28.2.194",
            "multi-domain-server": "Firewall-ivory-main-take-263",
            "active": true
          },
          {
            "name": "SMS_Server_2",
            "type": "management server",
            "ipv4-address": "172.28.2.196",
            "multi-domain-server": "site-b",
            "active": false
          }
        ],
        "global-domain-assignments": []
      }
    }
  ]
}
```
