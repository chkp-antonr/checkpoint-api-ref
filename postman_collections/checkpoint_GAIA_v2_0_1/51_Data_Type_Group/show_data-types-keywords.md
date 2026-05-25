# show data-types-keywords

**Collection:** Web API (version 2.0.1) > 51 Data Type Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show data-types-keywords`

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

### Example 1: show data-types-keywords
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 9,
  "total": 9,
  "objects": [
    {
      "uid": "45724c70-18c7-49d3-8341-fca9a5208192",
      "name": "Certificate Signing Request File",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "4daf18a6-7959-493f-ad01-aab8bf98d4ef",
      "name": "DSA Private Key",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "710781c1-5611-4b48-aab4-5d39341232ef",
      "name": "keywords_obj",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "484f62e0-55cf-4ab5-ad1c-54881b045286",
      "name": "Multinational Terms for Secret",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "5c213c2b-7b72-4f9f-ab9c-244ab58ca997",
      "name": "Multinational Terms for Top Secret",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "8cd4163f-a311-4296-8d18-82608f3622b5",
      "name": "PGP Private Key",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "ee9b40c7-17d1-4b07-9e71-23d35b61cd67",
      "name": "RSA Private Key",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "37599fe8-8cdd-42f4-8f5d-23854fd466af",
      "name": "SSH Private Key",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    },
    {
      "uid": "d68bf987-1247-45a8-99ae-15a464f6f1c5",
      "name": "SSL or Privacy Enhanced Mail Certificate",
      "type": "data-type-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "navy blue"
    }
  ]
}
```
