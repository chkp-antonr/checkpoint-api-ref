# set-data-center-query set Data Center Servers to All

**Collection:** Web API (version 2.1) > 75 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-center-query`

## Description

Set All Data Centers for a Data Center Query

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "data-centers": {
    "set": "All"
  },
  "name": "data-center-query1"
}
```

## Example Responses

### Example 1: set-data-center-query set Data Center Servers to All
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8024422d-74c2-487e-a196-a8649e3f88da",
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
      "posix": 1591519435090,
      "iso-8601": "2020-06-07T11:43+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1591513615720,
      "iso-8601": "2020-06-07T10:06+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataSource",
  "query-rules": [
    {
      "uid": "20387286-f498-4620-a5fb-7de596ba721c",
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
      "icon": "NetworkObjects/ExternalDataSource",
      "key-type": "PREDEFINED",
      "key": "name-in-data-center",
      "values": [
        "myvalue"
      ]
    }
  ],
  "data-centers": [],
  "using-all-data-center": true
}
```
