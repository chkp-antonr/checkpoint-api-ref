# clone-resource-cifs

**Collection:** Web API (version 2.1) > 49 Resource CIFS
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-resource-cifs`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "api_cif"
}
```

## Example Responses

### Example 1: clone-resource-cifs
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b9e08434-c494-4663-9c7c-7fbc2135bc87",
  "name": "api_cif_Clone",
  "type": "resource-cifs",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1661350695454,
      "iso-8601": "2022-08-24T17:18+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661350695454,
      "iso-8601": "2022-08-24T17:18+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "log-mapped-shares": true,
  "log-access-violation": false,
  "block-remote-registry-access": true,
  "allowed-disk-and-print-shares": [
    {
      "server-name": "server20",
      "share-name": "share20"
    },
    {
      "server-name": "server3",
      "share-name": "share3"
    }
  ]
}
```
