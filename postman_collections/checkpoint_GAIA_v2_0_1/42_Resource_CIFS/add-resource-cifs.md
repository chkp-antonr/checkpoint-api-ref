# add-resource-cifs

**Collection:** Web API (version 2.0.1) > 42 Resource CIFS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-resource-cifs`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newCifsResource",
  "allowed-disk-and-print-shares": [
    {
      "server-name": "server1",
      "share-name": "share1"
    },
    {
      "server-name": "server2",
      "share-name": "share2"
    }
  ]
}
```

## Example Responses

### Example 1: add-resource-cifs
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "50c2789b-e565-48d4-9dc5-cb68da8966b3",
  "name": "newCifsResource",
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
      "posix": 1661238221683,
      "iso-8601": "2022-08-23T10:03+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661238221683,
      "iso-8601": "2022-08-23T10:03+0300"
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
      "server-name": "server1",
      "share-name": "share1"
    },
    {
      "server-name": "server2",
      "share-name": "share2"
    }
  ]
}
```
