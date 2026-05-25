# show-dns-domain

**Collection:** Web API (version 2.0.1) > 20 DNS Domain
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-dns-domain`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": ".www.example.com"
}
```

## Example Responses

### Example 1: show-dns-domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ab7aa902-ccac-4278-b4eb-c140c07c6170",
  "name": ".www.example.com",
  "type": "dns-domain",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1478675839059,
      "iso-8601": "2016-11-09T09:17+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1478675839059,
      "iso-8601": "2016-11-09T09:17+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/domain",
  "is-sub-domain": false
}
```
