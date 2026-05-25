# show-radius-groups

**Collection:** Web API (version 2.1) > 33 RADIUS Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-radius-groups`

## Description

Show Radius groups

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 4,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-radius-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 4,
  "total": 4,
  "objects": [
    {
      "uid": "cc17f634-00a9-4b9d-8c0b-2a3c700a3413",
      "name": "myspecialgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "2919ab66-4e95-4025-8492-6ffa6c8f0c38",
      "name": "newgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "ee5c2c89-d2e9-4b49-a3e5-96ef480be746",
      "name": "radgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    },
    {
      "uid": "51c85bec-4013-48eb-b5f8-ac25b2244002",
      "name": "testgroup",
      "type": "radius-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/group",
      "color": "black"
    }
  ]
}
```
