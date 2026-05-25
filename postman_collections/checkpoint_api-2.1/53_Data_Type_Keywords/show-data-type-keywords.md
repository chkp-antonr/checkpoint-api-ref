# show-data-type-keywords

**Collection:** Web API (version 2.1) > 53 Data Type Keywords
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-type-keywords`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "keywords_obj"
}
```

## Example Responses

### Example 1: show-data-type-keywords
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
