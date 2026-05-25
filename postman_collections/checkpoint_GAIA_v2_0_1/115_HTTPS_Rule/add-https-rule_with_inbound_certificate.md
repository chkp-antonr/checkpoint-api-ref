# add-https-rule with inbound certificate

**Collection:** Web API (version 2.0.1) > 115 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Default Layer",
  "position": 1,
  "name": "CertificateRule",
  "source": "internet",
  "destination": "MyServer",
  "action": "Inspect",
  "certificate": "MyServerCertificate"
}
```

## Example Responses

### Example 1: add-https-rule with inbound certificate
**Status:** `200 OK`
