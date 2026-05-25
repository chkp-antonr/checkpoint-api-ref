# add-multiple-key-exchanges (with multiple algorithms)

**Collection:** Web API (version 2.0.1) > 100 Multiple Key Exchanges
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-multiple-key-exchanges`

## Description

Adds a new Multiple Key Exchanges with multiple algorithms options.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Multiple Key Exchanges2",
  "key-exchange-methods": "group-2",
  "additional-key-exchange-1-methods": [
    "kyber-768",
    "kyber-1024"
  ]
}
```

## Example Responses

### Example 1: add-multiple-key-exchanges (with multiple algorithms)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "55cb72bd-9d62-4418-8974-0cb1e9072d4c",
  "name": "Multiple Key Exchanges2",
  "type": "multiple-key-exchanges",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1706106407537,
      "iso-8601": "2024-01-24T16:26+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1706106407537,
      "iso-8601": "2024-01-24T16:26+0200"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa",
  "key-exchange-methods": [
    "group-2"
  ],
  "additional-key-exchange-1-methods": [
    "kyber-768",
    "kyber-1024"
  ],
  "additional-key-exchange-2-methods": [],
  "additional-key-exchange-3-methods": [],
  "additional-key-exchange-4-methods": [],
  "additional-key-exchange-5-methods": [],
  "additional-key-exchange-6-methods": [],
  "additional-key-exchange-7-methods": []
}
```
