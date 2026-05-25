# show-data-types-weighted-keywords

**Collection:** Web API (version 2.0.1) > 48 Data Type Weighted-Keywords
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-data-types-weighted-keywords`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5
}
```

## Example Responses

### Example 1: show-data-types-weighted-keywords
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 5,
  "total": 16,
  "objects": [
    {
      "uid": "9da238f7-72f2-452a-9d6a-2fdbe6988940",
      "name": "adam_words",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "black"
    },
    {
      "uid": "d5011231-f943-4f53-8d76-0f60c3c07f71",
      "name": "my_words",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "orange"
    },
    {
      "uid": "565cad8a-9da7-41f7-bdcb-1b51bcd1f697",
      "name": "Source Code - ActionScript",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "gold"
    },
    {
      "uid": "4ff942f3-6087-46b0-ad52-c17a2837cfdc",
      "name": "Source Code - ASP",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "gold"
    },
    {
      "uid": "3447e774-e688-45b6-89ea-3eeae645ec96",
      "name": "Source Code - ASP dot NET",
      "type": "data-type-weighted-keywords",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/Data_Object",
      "color": "gold"
    }
  ]
}
```
