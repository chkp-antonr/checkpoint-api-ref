# show-data-center-server

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-data-center-server`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vCenter 1"
}
```

## Example Responses

### Example 1: show-data-center-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d5379ada-c7d7-4678-bf55-0776f33b2326",
  "name": "vCenter 1",
  "type": "data-center-server",
  "domain": {
    "domain-type": "domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1454506141609,
      "iso-8601": "2016-02-03T08:29-0500"
    },
    "last-modifier": "admin",
    "creation-time": {
      "posix": 1454506141609,
      "iso-8601": "2016-02-03T08:29-0500"
    },
    "creator": "admin"
  },
  "tags": [],
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataSource",
  "server-type": "vcenter",
  "properties": {
    "username": "user1",
    "hostname": "vcenter1.host.com"
  }
}
```
