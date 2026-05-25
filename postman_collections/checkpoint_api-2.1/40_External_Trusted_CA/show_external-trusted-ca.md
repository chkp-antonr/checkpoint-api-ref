# show external-trusted-ca

**Collection:** Web API (version 2.1) > 40 External Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-external-trusted-ca`

## Description

Show external trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "external_ca"
}
```

## Example Responses

### Example 1: show external-trusted-ca
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "bae2e0c7-4667-49a8-95c7-1ce9d7cd6584",
  "name": "external_ca",
  "type": "external-trusted-ca",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1703162491765,
      "iso-8601": "2023-12-21T14:41+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1703162491765,
      "iso-8601": "2023-12-21T14:41+0200"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIICujCCAaKgAwIBAgIIP1+IHWHbl0EwDQYJKoZIhvcNAQELBQAwFDESMBAGA1UE\nAxMJd3d3LnouY29tMB4XDTIzMTEyOTEyMzAwMFoXDTI0MTEyMDE2MDAwMFowFDES\nMBAGA1UEAxMJd3d3LnouY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKC\nAQEAoBreRGuq8u43GBog+ZaAnaR8ZF8cT2ppvtd3JoFmzTOQivLIt9sNtFYqEgHC\ntnNkKn9TRrxN14YscHgKIxfDSVlC9Rh0rrBvWgFqcm715Whr99Ogx6JbYFkusFWJ\narSejIFx4n6MM48MJxLdtCP6Hy1G2cj1BCiCHj4i3VIVaDE/aMkSqJbYEvf+vFqU\nWxY8/uEuKI/HGhI7mhUPW4NSGL0Oafz5eEFVsxqV5NA19/JJZ9NajSkyANnaNL5r\naxGV0oeqaE3JB3lSEZfWbH6mQsToUxxwIQfsZiIBozajDdTgP3Kn4SMY0b+I/WAW\ngfigMSDTAIR8J1sdzGXy2w2kqQIDAQABoxAwDjAMBgNVHRMEBTADAQH/MA0GCSqG\nSIb3DQEBCwUAA4IBAQBUgrHztHwC1E0mU5c4reMrHg+z+YRHrgJNHVIYQbL5I2TJ\nHk9S3UZsynoMa1CO86rReOtR5xoGv4PCkyyOW+PNlWUtXF3tNgqWj/21+XzG4RBH\nPw89TaTxRCdo+MHX58fi07SIzKjmxfdkEi+7+HQEQluDZGViolrGBAw2rXq/SZ3q\n/11mNqlb5ZyqyOa2u1sBF1ApvG5a/FBRTaO8gaiNelRf0PGYkuV+1HhF2XyP8Qk5\n65d+uxUH5M7eHF2PNyVk/r/36T+x+UMql9y9iizA0ekuAjXLok1xYl3Vw4S5zXCX\nYtNZLOVrs+plJb7IrlElyTOAbDFuPugh0medz7uZ\n-----END CERTIFICATE-----\n",
  "retrieve-crl-from-http-servers": true,
  "retrieve-crl-from-ldap-servers": false,
  "cache-crl": true,
  "crl-cache-method": "timeout",
  "crl-cache-timeout": 1440,
  "allow-certificates-from-branches": false,
  "branches": []
}
```
