# add securemote-dns-server

**Collection:** Web API (version 2.1) > 42 SecuRemote DNS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-securemote-dns-server`

## Description

Adds new SecuRemote DNS server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSecuRemoteDNSSever",
  "host": "TestHost",
  "domains": [
    {
      "domain-suffix": ".FirstDomain",
      "maximum-prefix-label-count": 3
    },
    {
      "domain-suffix": ".SecondDomain"
    }
  ]
}
```

## Example Responses

### Example 1: add securemote-dns-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2851178b-d315-4687-b48d-eb45b656e14f",
  "name": "TestSecuRemoteDNSSever",
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
      "posix": 1746457746950,
      "iso-8601": "2025-05-05T18:09+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1746457746950,
      "iso-8601": "2025-05-05T18:09+0300"
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
    "uid": "839a5757-d814-4f9a-8684-a5becf5d9b9f",
    "name": "TestHost",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "icon": "Objects/host",
    "color": "black",
    "ipv4-address": "1.1.1.1"
  },
  "domains": [
    {
      "domain-suffix": ".FirstDomain",
      "maximum-prefix-label-count": 3
    },
    {
      "domain-suffix": ".SecondDomain",
      "maximum-prefix-label-count": 1
    }
  ]
}
```
