# show-updatable-objects

**Collection:** Web API (version 2.0.1) > 67 Updatable Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-updatable-objects`

## Description

Shows all the imported updatable objects

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

### Example 1: show-updatable-objects
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "63a04b20-8e4f-4282-8224-69252c3495e1",
      "name": "Amazon AP North-East 1",
      "type": "updatable-object",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "1506cdeb-c132-4d28-bca5-95eb07e12828",
      "name": "CodeBuild US East 1",
      "type": "updatable-object",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
