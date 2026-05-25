# show-data-type-compound-groups

**Collection:** Web API (version 2.1) > 59 Data Type Compound Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-type-compound-groups`

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

### Example 1: show-data-type-compound-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 4,
  "total": 4,
  "objects": [
    {
      "uid": "eff8261a-92a8-46a2-85d3-f5242f176c31",
      "name": "compound-group-obj",
      "type": "data-type-compound-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "6c2e25f9-5e32-439a-a678-7614b29234c7",
      "name": "PCI - Credit Card Numbers - 20 or more",
      "type": "data-type-compound-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "69c3ac77-18a3-42e0-ae3f-6152fa705610",
      "name": "PCI - Credit Card Numbers - 5 or more",
      "type": "data-type-compound-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "bcdffac3-193a-473d-b8c6-a1ac4420c968",
      "name": "Salary Survey Report",
      "type": "data-type-compound-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "sienna"
    }
  ]
}
```
