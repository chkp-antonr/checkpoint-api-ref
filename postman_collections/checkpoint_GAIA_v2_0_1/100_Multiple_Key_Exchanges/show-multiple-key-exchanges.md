# show-multiple-key-exchanges

**Collection:** Web API (version 2.0.1) > 100 Multiple Key Exchanges
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-multiple-key-exchanges`

## Description

Show an existing Multiple Key Exchanges.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Multiple Key Exchanges"
}
```

## Example Responses

### Example 1: show-multiple-key-exchanges
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5c25c4c4-4fc5-4371-b0f5-ab2473c6a69b",
  "name": "Multiple Key Exchanges",
  "type": "multiple-key-exchanges",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1706107045308,
      "iso-8601": "2024-01-24T16:37+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1706106606362,
      "iso-8601": "2024-01-24T16:30+0200"
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
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa",
  "key-exchange-methods": [
    "group-2"
  ],
  "additional-key-exchange-1-methods": [
    "kyber-768"
  ],
  "additional-key-exchange-2-methods": [],
  "additional-key-exchange-3-methods": [],
  "additional-key-exchange-4-methods": [],
  "additional-key-exchange-5-methods": [],
  "additional-key-exchange-6-methods": [],
  "additional-key-exchange-7-methods": []
}
```
