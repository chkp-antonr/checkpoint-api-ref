# set-resource-cifs

**Collection:** Web API (version 2.1) > 49 Resource CIFS
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-resource-cifs`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newCifsResource3",
  "allowed-disk-and-print-shares": [
    {
      "server-name": "server5",
      "share-name": "share5"
    },
    {
      "server-name": "server6",
      "share-name": "share6"
    }
  ]
}
```

## Example Responses

### Example 1: set-resource-cifs
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ea1a9749-f4d3-4d96-823f-3acca981243e",
  "name": "newCifsResource3",
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
      "posix": 1661257084323,
      "iso-8601": "2022-08-23T15:18+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661253024202,
      "iso-8601": "2022-08-23T14:10+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "log-mapped-shares": false,
  "log-access-violation": false,
  "block-remote-registry-access": true,
  "allowed-disk-and-print-shares": [
    {
      "server-name": "server5",
      "share-name": "share5"
    },
    {
      "server-name": "server6",
      "share-name": "share6"
    }
  ]
}
```
