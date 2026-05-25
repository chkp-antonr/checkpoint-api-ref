# add-data-type-keywords

**Collection:** Web API (version 2.0.1) > 46 Data Type Keywords
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-type-keywords`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "keywords_obj",
  "description": "keywords object",
  "keywords.1": "word1",
  "keywords.2": "word2",
  "data-match-threshold": "all-keywords"
}
```

## Example Responses

### Example 1: add-data-type-keywords
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6f6032c4-7b41-448e-92fc-98d47b357cbc",
  "name": "keywords_obj",
  "type": "data-type-keywords",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695665514865,
      "iso-8601": "2023-09-25T21:11+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695665514865,
      "iso-8601": "2023-09-25T21:11+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "keywords object",
  "keywords": [
    "word1",
    "word2"
  ],
  "data-match-threshold": "all-keywords",
  "min-number-of-keywords": 1
}
```
