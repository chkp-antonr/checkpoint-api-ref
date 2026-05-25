# set-data-center-query set query rules

**Collection:** Web API (version 2.0.1) > 64 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-data-center-query`

## Description

Set new query rules

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
    "key": "name-in-data-center",
    "key-type": "predefined",
    "values": [
      "myName2"
    ]
  }
}
```

## Example Responses

### Example 1: set-data-center-query set query rules
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "27462eb6-f386-48b3-8986-12aaa56b587d",
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
      "posix": 1594640753251,
      "iso-8601": "2020-07-13T14:45+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1594640634151,
      "iso-8601": "2020-07-13T14:43+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataQuery",
  "query-rules": [
    {
      "uid": "832c3f41-7e2d-4223-9357-6e661c32dea1",
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
        "myName2"
      ]
    }
  ],
  "data-centers": [],
  "using-all-data-center": true
}
```
