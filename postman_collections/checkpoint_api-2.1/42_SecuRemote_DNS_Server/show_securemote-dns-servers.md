# show securemote-dns-servers

**Collection:** Web API (version 2.1) > 42 SecuRemote DNS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-securemote-dns-servers`

## Description

Retrieve all Securemote DNS servers.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5,
  "offset": 0,
  "details-level": "full"
}
```

## Example Responses

### Example 1: show securemote-dns-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
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
          "posix": 1746457943981,
          "iso-8601": "2025-05-05T18:12+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746457746967,
          "iso-8601": "2025-05-05T18:09+0300"
        },
        "creator": "WEB_API"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "tags": [],
      "read-only": false,
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1746457918528,
            "iso-8601": "2025-05-05T18:11+0300"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1746457918528,
            "iso-8601": "2025-05-05T18:11+0300"
          },
          "creator": "WEB_API"
        },
        "available-actions": {
          "edit": "true",
          "delete": "true",
          "clone": "true"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "Objects/host",
        "groups": [],
        "nat-settings": {
          "auto-rule": false
        },
        "ipv4-address": "2.2.2.2",
        "interfaces": []
      },
      "domains": [
        {
          "domain-suffix": ".ThirdDomain",
          "maximum-prefix-label-count": 2
        }
      ]
    },
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
          "posix": 1746458152166,
          "iso-8601": "2025-05-05T18:15+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746458152166,
          "iso-8601": "2025-05-05T18:15+0300"
        },
        "creator": "WEB_API"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "tags": [],
      "read-only": false,
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1746457918528,
            "iso-8601": "2025-05-05T18:11+0300"
          },
          "last-modifier": "WEB_API",
          "creation-time": {
            "posix": 1746457918528,
            "iso-8601": "2025-05-05T18:11+0300"
          },
          "creator": "WEB_API"
        },
        "available-actions": {
          "edit": "true",
          "delete": "true",
          "clone": "true"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "Objects/host",
        "groups": [],
        "nat-settings": {
          "auto-rule": false
        },
        "ipv4-address": "2.2.2.2",
        "interfaces": []
      },
      "domains": [
        {
          "domain-suffix": ".ThirdDomain",
          "maximum-prefix-label-count": 2
        }
      ]
    }
  ]
}
```
