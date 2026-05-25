# show-object

**Collection:** Web API (version 2.1) > 183 Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-object`

## Description

Show object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "ef82887c-d08f-49a3-a18f-a376be633848"
}
```

## Example Responses

### Example 1: show-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "object": {
    "folder": {
      "uid": "a25a7783-9adb-4a65-9850-b97ee7860530",
      "name": "/Global Objects"
    },
    "domain": {
      "domain-type": "local domain",
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User"
    },
    "type": "ThreatRulebase",
    "name": "ThreatStandard",
    "uid": "ef82887c-d08f-49a3-a18f-a376be633848"
  }
}
```
