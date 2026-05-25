# show-data-type-traditional-groups

**Collection:** Web API (version 2.1) > 57 Data Type Traditional Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-type-traditional-groups`

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

### Example 1: show-data-type-traditional-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 8,
  "total": 8,
  "objects": [
    {
      "uid": "2f0fae3b-dab5-4b85-b85a-d7e1e4a8e0e6",
      "name": "Certificate Files",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "0c559c29-3940-4814-8cdb-5fa204fe04a4",
      "name": "Certificates and Private Keys",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "68ad2a74-9fe2-4a79-ace8-88220d4b4072",
      "name": "Credit Card Numbers or IBAN",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "1a6fd4f2-4d89-4d06-9fa6-fb35d5c6a447",
      "name": "PCI - Magnetic Stripe Data",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "1e570241-f1e3-47cf-ab8b-97e0eb86f051",
      "name": "Private Key Files",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "a962244d-5086-4d82-a5d6-322ff8deeeb6",
      "name": "Source Code",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "gold"
    },
    {
      "uid": "0065b876-40b9-46fe-b165-1a8a9c3ca785",
      "name": "Spreadsheet or CSV File",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "be7f94fb-1a57-46a5-938e-ca557d816bf4",
      "name": "trad-group-obj",
      "type": "data-type-traditional-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    }
  ]
}
```
