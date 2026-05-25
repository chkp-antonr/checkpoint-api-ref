# show-data-center-query

**Collection:** Web API (version 2.1) > 75 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-center-query`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "data-center-query1"
}
```

## Example Responses

### Example 1: show-data-center-query
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a7c905bd-04e9-47d0-b6c2-91f49ee8b5af",
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
      "posix": 1591266428871,
      "iso-8601": "2020-06-04T13:27+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1591088154952,
      "iso-8601": "2020-06-02T11:55+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataSource",
  "query-rules": [
    {
      "uid": "f967e4b0-50a5-46d2-9cdb-aed7cf4d44e8",
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
      "key": "IP Address",
      "values": [
        "10.0.0.1"
      ]
    }
  ],
  "data-centers": [
    {
      "uid": "088d2439-5c0c-4223-a9ca-afc7da9df4d2",
      "name": "AWS",
      "type": "data-center-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ],
  "using-all-data-center": true
}
```
