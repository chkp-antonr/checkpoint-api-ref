# add-data-center-query key-type tag

**Collection:** Web API (version 2.0.1) > 64 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-center-query`

## Description

Adds new data center query with tag query rule

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "data-center-query1",
  "query-rules": {
    "key-type": "tag",
    "key": "tag key",
    "values": [
      "tag value"
    ]
  }
}
```

## Example Responses

### Example 1: add-data-center-query key-type tag
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "08a3d6c6-0253-4f41-9e83-611690b3af24",
  "name": "data-center-query1",
  "type": "data-center-query",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1592390781091,
      "iso-8601": "2020-06-17T13:46+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1592390781091,
      "iso-8601": "2020-06-17T13:46+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataQuery",
  "query-rules": [
    {
      "uid": "c59a085c-5025-49a7-a887-db34eb25d1ad",
      "type": "DataCenterQueryRule",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok"
      },
      "tags": [],
      "read-only": true,
      "comments": "",
      "color": "black",
      "icon": "NetworkObjects/ExternalDataQuery",
      "key-type": "TAG",
      "key": "tag key",
      "values": [
        "tag value"
      ]
    }
  ],
  "data-centers": [],
  "using-all-data-center": true
}
```
