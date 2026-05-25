# show-mobile-profiles

**Collection:** Web API (version 2.0.1) > 85 Mobile Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-mobile-profiles`

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

### Example 1: show-mobile-profiles
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "c548188a-863c-4d20-83bb-a62972ca1878",
      "name": "Default_Profile",
      "type": "mobile-profile",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "MobileProfile/mobile_profile",
      "color": "black"
    },
    {
      "uid": "b1473db6-97d6-4241-b5da-7f41f11d3349",
      "name": "New Mobile Profile",
      "type": "mobile-profile",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "MobileProfile/mobile_profile",
      "color": "black"
    }
  ]
}
```
