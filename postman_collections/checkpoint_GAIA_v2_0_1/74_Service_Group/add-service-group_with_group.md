# add-service-group with group

**Collection:** Web API (version 2.0.1) > 74 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Service Group 3",
  "members": [
    "https"
  ],
  "groups": [
    "My Service Group1",
    "My Service Group2"
  ]
}
```

## Example Responses

### Example 1: add-service-group with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "dce67d0d-5efe-4808-b22d-2eb99e24c70d",
  "folder": {
    "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
    "name": "/Global Objects"
  },
  "domain": {
    "domain-type": "local domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1435472557082,
      "iso-8601": "2015-06-28T09:22+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1435472557082,
      "iso-8601": "2015-06-28T09:22+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Service Group 3",
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [
    {
      "folder": {
        "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "service-group",
      "name": "My Service Group1",
      "uid": "70600af1-3e61-41e2-b031-d46b2a171f86"
    },
    {
      "folder": {
        "uid": "5568324a-68ed-4c6c-9aa6-553978c7e746",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "service-group",
      "name": "My Service Group2",
      "uid": "e971be7e-8372-475f-9863-c0b0c5285cc0"
    }
  ],
  "members": [
    {
      "folder": {
        "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
        "name": "Global Objects"
      },
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "service-tcp",
      "name": "https",
      "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30"
    }
  ]
}
```
