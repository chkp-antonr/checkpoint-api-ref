# clone-application-site-group

**Collection:** Web API (version 2.1) > 88 Application Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-application-site-group`

## Description

Clone existing application site group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Group 1"
}
```

## Example Responses

### Example 1: clone-application-site-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0b7d5ba3-b908-4d54-bde8-4b730f0ad7a2",
  "name": "New Application Site Group 1_Clone",
  "type": "application-site-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747514892178,
      "iso-8601": "2025-05-17T23:48+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1747514892178,
      "iso-8601": "2025-05-17T23:48+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/group",
  "groups": [],
  "members": [
    {
      "uid": "40ea63ba-5d27-4269-b5de-ac8e6910872e",
      "name": "New Application Site Category 1",
      "type": "application-site-category",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/category",
      "color": "black"
    },
    {
      "uid": "00fa9e3d-4924-0f65-e053-08241dc22da2",
      "name": "Facebook",
      "type": "application-site",
      "domain": {
        "uid": "8bf4ac51-2df7-40e1-9bce-bedbedbedbed",
        "name": "APPI Data",
        "domain-type": "data domain"
      },
      "icon": "@app/10080872_2",
      "color": "black"
    },
    {
      "uid": "7c29f570-99a5-4455-915b-a3caa946efab",
      "name": "New Application Site 1",
      "type": "application-site",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/application",
      "color": "black"
    },
    {
      "uid": "00fa9e44-4165-0f65-e053-08241dc22da2",
      "name": "Social Networking",
      "type": "application-site-category",
      "domain": {
        "uid": "8bf4ac51-2df7-40e1-9bce-bedbedbedbed",
        "name": "APPI Data",
        "domain-type": "data domain"
      },
      "icon": "Objects/category",
      "color": "black"
    }
  ]
}
```
