# add-application-site-group with group

**Collection:** Web API (version 2.1) > 88 Application Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-application-site-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Group 3",
  "members": [
    "facebook",
    "Social Networking"
  ],
  "groups": [
    "New Application Site Group 1",
    "New Application Site Group 2"
  ]
}
```

## Example Responses

### Example 1: add-application-site-group with group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "78a80391-c8d3-4317-8938-82de07424421",
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
      "posix": 1435473044262,
      "iso-8601": "2015-06-28T09:30+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1435473044262,
      "iso-8601": "2015-06-28T09:30+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Application Site Group 3",
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
      "type": "application-site-group",
      "name": "New Application Site Group 1",
      "uid": "bdcdb02b-c3d4-4aa6-98d5-cf6da1f09eb1"
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
      "type": "application-site-group",
      "name": "New Application Site Group 2",
      "uid": "dab93684-b276-44ce-bcd5-4d7796d15fe0"
    }
  ],
  "members": [
    {
      "folder": {
        "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
        "name": "Check Point Settings"
      },
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "application-site",
      "name": "Facebook",
      "uid": "00fa9e3d-4924-0f65-e053-08241dc22da2"
    },
    {
      "folder": {
        "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
        "name": "Check Point Settings"
      },
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "application-site-category",
      "name": "Social Networking",
      "uid": "00fa9e44-4165-0f65-e053-08241dc22da2"
    }
  ]
}
```
