# set-data-type-patterns

**Collection:** Web API (version 2.1) > 56 Data Type Patterns
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-type-patterns`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "pattern-obj",
  "patterns.remove.1": "^d",
  "number-of-occurrences": 3
}
```

## Example Responses

### Example 1: set-data-type-patterns
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7d6e8f77-0f08-49c4-b5d0-4bcf4af9fec7",
  "name": "pattern-obj",
  "type": "data-type-patterns",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1695707213756,
      "iso-8601": "2023-09-26T08:46+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1695675954788,
      "iso-8601": "2023-09-26T00:05+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/Data_Object",
  "description": "data type pattern object",
  "patterns": [
    "a*b"
  ],
  "number-of-occurrences": 3
}
```
