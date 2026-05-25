# show-outbound-inspection-certificates

**Collection:** Web API (version 2.1) > 130 Outbound Inspection Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-outbound-inspection-certificates`

## Description

Show all outbound certificates objects.

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

### Example 1: show-outbound-inspection-certificates
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 50,
  "total": 2,
  "objects": [
    {
      "uid": "3b400e12-e213-4111-a256-2c962d5cf6fa",
      "name": "OutboundCertificate",
      "type": "outbound-inspection-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "subject_user_certificate",
      "color": "black"
    },
    {
      "uid": "3766347c-7085-4bc3-8f5e-4a5a95334a5b",
      "name": "OutboundCertificate1",
      "type": "outbound-inspection-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "subject_user_certificate",
      "color": "black"
    }
  ]
}
```
