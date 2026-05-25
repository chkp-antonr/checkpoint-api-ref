# unlock access-rule using name, type and layer

**Collection:** Web API (version 2.0.1) > 165 Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/unlock-object`

## Description

Unlock rule using name, type and layer.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "rule2",
  "type": "access-rule",
  "layer": "Network"
}
```

## Example Responses

### Example 1: unlock access-rule using name, type and layer
**Status:** `200 OK`

**Body:**
```javascript
{
  "object": {
    "uid": "77383541-a9b1-48ed-bec6-6eebae1f2d1f",
    "name": "rule2",
    "type": "access-rule",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    }
  }
}
```
