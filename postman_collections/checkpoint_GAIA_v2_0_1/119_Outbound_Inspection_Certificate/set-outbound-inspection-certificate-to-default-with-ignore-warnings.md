# set-outbound-inspection-certificate-to-default-with-ignore-warnings

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
  "is-default": "true",
  "ignore-warnings": "true"
}
```

## Example Responses

### Example 1: set-outbound-inspection-certificate-to-default-with-ignore-warnings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "17cfb93c-c1a2-46c7-ad26-5f183becf1cb",
  "name": "OutboundCertificate1",
  "type": "outbound-inspection-certificate",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1679907451970,
      "iso-8601": "2023-03-27T11:57+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1679907451970,
      "iso-8601": "2023-03-27T11:57+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "icon": "subject_user_certificate",
  "issued-by": "CN=www.checkpoint.com",
  "valid-from": "17-May-21",
  "valid-to": "17-May-28",
  "base64-certificate": "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",
  "public-certificate": "-----BEGIN CERTIFICATE-----\nMIIC2DCCAcCgAwIBAgIEL0zULjANBgkqhkiG9w0BAQsFADAdMRswGQYDVQQDExJ3\r\nd3cuY2hlY2twb2ludC5jb20wHhcNMjEwNTE2MjEwMDAwWhcNMjgwNTE2MjEwMDAw\r\nWjAdMRswGQYDVQQDExJ3d3cuY2hlY2twb2ludC5jb20wggEiMA0GCSqGSIb3DQEB\r\nAQUAA4IBDwAwggEKAoIBAQCxyCWt4sZKMxQEsVv1uB1T55aOkdTGEiqFTbA7TH7M\r\n8REqqLA0UPresOk8s7m06fuWC6jxeUjUqxGx/392CX3cZebYsQyeYqPZzS7rn3MO\r\nHfEY3Fq3Zpa57eJGG7lzjMetnCzOgG7YXgosTNIGT0C/W1RgLwMqghk9giJwuq5N\r\nYBeIa3z4bpVUULRT5EYu7SQ5fzYDmMgFsJ0hVt2eUKSTbZW4SMO+a1IoiPx+ESAB\r\nb5u4gv2+Jo3xd8FME8uoGPMNDoEU/Q/jjJWNtQsetrmlNGrHXKMLq/1/3h3s78AQ\r\nc5mKkb3WmLrPAi1jOifF9qwxkFYmBVaubmA5dxi0n2C3AgMBAAGjIDAeMA8GA1Ud\r\nEwEB/wQFMAMBAf8wCwYDVR0PBAQDAgGGMA0GCSqGSIb3DQEBCwUAA4IBAQA/R1DI\r\nhc1PHzEjsW9KxIf7ZcfZP6KL0g70emB6PsV+EGzIzXQySFv7d/FX52kvHndrLOMI\r\nUNspN+uwXd8xsWCV1Gp88A5xm35l+n2gRoBX0111V58Lj66m8Il+/6OsQDHTo+Ec\r\niFZhTfOpUmUTIPi3Xut/biIoqGJHPGTFE4Ofu1snNmPnsOhsq2c7FN99f++dFIyG\r\nIHJ2HyvPty8AuxV8RSbbiMcvvnceeXCa6NVpt6WTGeJwsbZXAkO39HgLrr8vflRv\r\nB9J0HISc3bYHc5yCtk/z0z+Dr+o7jYj+RfTXtgYBPikbJUsCJepF8kq8qNZWLkCZ\r\nSDFOf0seaSkqW2Dv\r\n-----END CERTIFICATE-----\n",
  "is-default": true
}
```
