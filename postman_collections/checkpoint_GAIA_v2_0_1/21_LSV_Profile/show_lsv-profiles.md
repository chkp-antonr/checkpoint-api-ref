# show lsv-profiles

**Collection:** Web API (version 2.0.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-lsv-profiles`

## Description

Display all LSV Profiles

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show lsv-profiles
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "5df51f76-744e-40cb-8957-64c9b95d6d52",
      "name": "Another lsv-profile",
      "type": "lsv-profile",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "0cb15fb6-f1a7-42d5-9eef-64aaef000642",
      "name": "New lsv-profile",
      "type": "lsv-profile",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
