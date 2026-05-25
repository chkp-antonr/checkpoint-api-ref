# show-multiple-key-exchanges-objects

**Collection:** Web API (version 2.0.1) > 100 Multiple Key Exchanges
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-multiple-key-exchanges-objects`

## Description

Show all Multiple Key Exchanges.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-multiple-key-exchanges-objects
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "5c25c4c4-4fc5-4371-b0f5-ab2473c6a69b",
      "name": "Multiple Key Exchanges",
      "type": "multiple-key-exchanges",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/globalsNa",
      "color": "black"
    }
  ]
}
```
