# set-data-type-keywords

**Collection:** Web API (version 2.1) > 53 Data Type Keywords
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-type-keywords`

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
  "keywords.1": "word3",
  "data-match-threshold": "min-keywords",
  "min-number-of-keywords": 3
}
```

## Example Responses

### Example 1: set-data-type-keywords
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "710781c1-5611-4b48-aab4-5d39341232ef",
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
      "posix": 1695668338353,
      "iso-8601": "2023-09-25T21:58+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695668269856,
      "iso-8601": "2023-09-25T21:57+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "keywords object",
  "keywords": [
    "word3"
  ],
  "data-match-threshold": "min-keywords",
  "min-number-of-keywords": 3
}
```
