# add-multiple-key-exchanges

**Collection:** Web API (version 2.1) > 111 Multiple Key Exchanges
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-multiple-key-exchanges`

## Description

Adds a new Multiple Key Exchanges.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Multiple Key Exchanges",
  "key-exchange-methods": "group-2",
  "additional-key-exchange-1-methods": "kyber-768"
}
```

## Example Responses

### Example 1: add-multiple-key-exchanges
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "fd98e646-ba75-4494-9147-277653b89664",
  "name": "Multiple Key Exchanges",
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
      "posix": 1706106278048,
      "iso-8601": "2024-01-24T16:24+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1706106278048,
      "iso-8601": "2024-01-24T16:24+0200"
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
