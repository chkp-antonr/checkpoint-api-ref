# show-override-categorization

**Collection:** Web API (version 2.0.1) > 79 Override Categorization
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-override-categorization`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "url": "newOverride"
}
```

## Example Responses

### Example 1: show-override-categorization
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "70c17128-5e5c-485e-ab4d-fb932816d2fd",
  "url": "newOverride",
  "type": "override-categorization",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1661343193510,
      "iso-8601": "2022-08-24T15:13+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661342747270,
      "iso-8601": "2022-08-24T15:05+0300"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comment": "",
  "color": "black",
  "icon": "Objects/application",
  "new-primary-category": {
    "uid": "00fa9e44-40b0-0f65-e053-08241dc22da2",
    "name": "Botnets",
    "type": "application-site-category",
    "domain": {
      "uid": "8bf4ac51-2df7-40e1-9bce-bedbedbedbed",
      "name": "APPI Data",
      "domain-type": "data domain"
    },
    "icon": "Objects/category",
    "color": "black"
  },
  "risk": "high",
  "additional-categories": [],
  "url-defined-as-regular-expression": false
}
```
