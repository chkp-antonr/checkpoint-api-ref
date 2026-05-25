# set-outbound-inspection-certificate-to-default

**Collection:** Web API (version 2.0.1) > 119 Outbound Inspection Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-outbound-inspection-certificate`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "OutboundCertificate",
  "new-name": "OutboundCertificate1",
  "issued-by": "www.checkpoint.com",
  "base64-password": "bXlfcGFzc3dvcmQ=",
  "valid-from": "2021-05-17",
  "valid-to": "2028-05-17",
  "is-default": "true"
}
```

## Example Responses

### Example 1: set-outbound-inspection-certificate-to-default
**Status:** `200 OK`

**Body:**
```javascript
{
  "code": "err_outbound_inspection_certificate_operation_failed",
  "message": "Default outbound certificate: c118da24-a234-4c27-80f9-aa53c0b55cef is about to be replaced"
}
```
