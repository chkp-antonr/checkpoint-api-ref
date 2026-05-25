# show-data-types-patterns

**Collection:** Web API (version 2.1) > 56 Data Type Patterns
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-types-patterns`

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

### Example 1: show-data-types-patterns
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 15,
  "total": 15,
  "objects": [
    {
      "uid": "1a4eccb6-31d6-458d-aa80-f73e038e241b",
      "name": "ABA Transit Numbers",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "eaae644f-e2fc-4401-829a-a7195a2b0fe3",
      "name": "CUSIP Number",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "e4c7b48b-4dfe-427a-853e-1a4226249950",
      "name": "HIPAA - Medical Record Number - MRN",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "8f057ffc-6a2e-492e-b0ab-596877ecf7bb",
      "name": "International Bank Account Number - IBAN",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "e4e524d3-4888-4575-a15a-9a452daf1723",
      "name": "International Securities Identification Number - ISIN",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "af92af6c-3a9c-4c2f-9040-c11c1b5770a8",
      "name": "IPI - Details of Payment Code",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "3ce61848-a025-4385-b92d-8d9773099302",
      "name": "MAC Address",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "11809b0f-a42f-438a-9886-1f532ebf41b4",
      "name": "Machine Readable Passport Numbers",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "red"
    },
    {
      "uid": "7d6e8f77-0f08-49c4-b5d0-4bcf4af9fec7",
      "name": "pattern-obj",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "16581df4-2c94-45d0-8203-0e8a72b43523",
      "name": "PCI - Credit Card Numbers",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "dark blue"
    },
    {
      "uid": "803a2243-961f-43f6-a527-ad1e5f5ca458",
      "name": "Personal Information Exchange File",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "5fc6b546-1ff7-460e-8dc0-608bdbfb7c66",
      "name": "SEDOL Codes",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    },
    {
      "uid": "4c55cff2-fd7b-4262-9e6d-a6f0ffe41245",
      "name": "SIM Serial Number - ICC-ID",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "red"
    },
    {
      "uid": "3d44e948-50ce-43a6-bd6c-bbdaa6775e26",
      "name": "U.S. Social Security Numbers - According to SSA",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "red"
    },
    {
      "uid": "87e7c6ab-729b-419d-bff0-7bdd06280c7a",
      "name": "Vehicle Identification Number - VIN",
      "type": "data-type-patterns",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "forest green"
    }
  ]
}
```
