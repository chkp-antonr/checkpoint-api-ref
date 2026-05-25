# show-threat-indicators

**Collection:** Web API (version 2.1) > 118 Threat Indicator
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-threat-indicators`

## Description

Showing a list of threat indicators

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

### Example 1: show-threat-indicators
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "indicators": [
    {
      "uid": "7c00fba4-978e-4769-acbf-46909b88f45d",
      "name": "My_Indicator",
      "type": "threat-indicator",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "4f797897-3109-43ec-9d07-340b74110f73",
      "name": "My_Indicator2",
      "type": "threat-indicator",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "c3bd4f1e-3df9-4b91-b2d9-5fc66428a520",
      "name": "My_Indicator3",
      "type": "threat-indicator",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
