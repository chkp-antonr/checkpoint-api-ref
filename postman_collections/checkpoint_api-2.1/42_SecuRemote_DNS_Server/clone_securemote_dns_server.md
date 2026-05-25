# clone securemote dns server

**Collection:** Web API (version 2.1) > 42 SecuRemote DNS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-securemote-dns-server`

## Description

Clone existing Securemote DNS server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSecuRemoteDNSSever"
}
```

## Example Responses

### Example 1: clone securemote dns server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2ff11558-57f9-4592-bbd1-5e29b63e3d90",
  "name": "TestSecuRemoteDNSSever_Clone",
  "type": "securemote-dns-server",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1746458152161,
      "iso-8601": "2025-05-05T18:15+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746458152161,
      "iso-8601": "2025-05-05T18:15+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "host": {
    "uid": "0ee12048-a8d3-4a11-9fd9-89825785b20b",
    "name": "TestHost2",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "2.2.2.2"
  },
  "domains": [
    {
      "domain-suffix": ".ThirdDomain",
      "maximum-prefix-label-count": 2
    }
  ]
}
```
