# show-data-center-objects

**Collection:** Web API (version 2.1) > 74 Data Center Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-center-objects`

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

### Example 1: show-data-center-objects
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 4,
  "total": 4,
  "objects": [
    {
      "uid": "61dcb32c-1c01-409d-bb04-f82b2faa5f00",
      "name": "VM1 mgmt name",
      "type": "data-center-object",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    },
    {
      "uid": "a0180380-2b1d-4ea8-b2be-865b76691261",
      "name": "My VM2",
      "type": "data-center-object",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    },
    {
      "uid": "115ba372-c70f-427e-ba64-6289f2fb67f9",
      "name": "My VM3",
      "type": "data-center-object",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    },
    {
      "uid": "406e7fc8-ab52-454a-9c9b-aa1cdbe97baf",
      "name": "My VM4",
      "type": "data-center-object",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    }
  ]
}
```
