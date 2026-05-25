# delete-outbound-inspection-certificate

**Collection:** Web API (version 2.1) > 130 Outbound Inspection Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-outbound-inspection-certificate`

## Description

Delete an outbound certificate object.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "OutboundCertificate"
}
```

## Example Responses

### Example 1: delete-outbound-inspection-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
