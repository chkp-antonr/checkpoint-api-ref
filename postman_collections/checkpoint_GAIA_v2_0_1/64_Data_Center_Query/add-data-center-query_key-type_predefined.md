# add-data-center-query key-type predefined

**Collection:** Web API (version 2.0.1) > 64 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-center-query`

## Description

Adds new data center query with predefined query rule

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
    "key-type": "predefined",
    "key": "name-in-data-center",
    "values": [
      "myName"
    ]
  }
}
```

## Example Responses

### Example 1: add-data-center-query key-type predefined
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f7db4afb-94a6-4bd2-b22f-8a77d6d4b9e1",
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
      "posix": 1592390598511,
      "iso-8601": "2020-06-17T13:43+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1592390598511,
      "iso-8601": "2020-06-17T13:43+0300"
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
      "uid": "973d064c-9df6-4b24-8b5b-a2e2db5ef60b",
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
      "key-type": "PREDEFINED",
      "key": "Name in Data Center",
      "values": [
        "myName"
      ]
    }
  ],
  "data-centers": [],
  "using-all-data-center": true
}
```
