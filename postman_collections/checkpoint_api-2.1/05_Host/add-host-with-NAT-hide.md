# add-host-with-NAT-hide

**Collection:** Web API (version 2.1) > 05 Host
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-host`

## Description

Adds simple host with NAT

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Host 3",
  "ip-address": "192.0.2.162",
  "nat-settings": {
    "auto-rule": true,
    "method": "hide",
    "hide-behind": "ip-address",
    "ipv4-address": "192.0.2.1",
    "install-on": "All"
  }
}
```

## Example Responses

### Example 1: add-host-with-NAT-hide
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "40048b5b-b64c-49ce-b8c7-267af43a0f9e",
  "name": "New Host 3",
  "type": "host",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1675943140554,
      "iso-8601": "2023-02-09T13:45+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1675943140554,
      "iso-8601": "2023-02-09T13:45+0200"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/host",
  "groups": [],
  "nat-settings": {
    "auto-rule": true,
    "ipv4-address": "192.0.2.1",
    "ipv6-address": "",
    "hide-behind": "ip-address",
    "method": "hide",
    "install-on": "All"
  },
  "ipv4-address": "192.0.2.162",
  "interfaces": []
}
```
