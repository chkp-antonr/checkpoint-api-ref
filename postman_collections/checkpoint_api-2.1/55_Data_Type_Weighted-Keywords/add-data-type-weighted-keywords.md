# add-data-type-weighted-keywords

**Collection:** Web API (version 2.1) > 55 Data Type Weighted-Keywords
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-type-weighted-keywords`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "weighted-words-obj",
  "weighted-keywords.1.keyword": "word1",
  "weighted-keywords.1.weight": 3,
  "weighted-keywords.1.max-weight": 4,
  "weighted-keywords.1.regex": true,
  "sum-of-weights-threshold": 10
}
```

## Example Responses

### Example 1: add-data-type-weighted-keywords
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "e9ddaf70-2694-49f7-b092-e068d4ecc32c",
  "name": "weighted-words-obj",
  "type": "data-type-weighted-keywords",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695673743339,
      "iso-8601": "2023-09-25T23:29+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695673743339,
      "iso-8601": "2023-09-25T23:29+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "weighted-keywords": [
    {
      "keyword": "word1",
      "weight": 3,
      "max-weight": 4,
      "regex": true
    }
  ],
  "sum-of-weights-threshold": 10
}
```
