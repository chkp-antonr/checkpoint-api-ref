# set internal-trusted-ca

**Collection:** Web API (version 2.1) > 39 Internal Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-internal-trusted-ca`

## Description

Set internal trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "retrieve-crl-from-http-servers": "false",
  "cache-crl": "false"
}
```

## Example Responses

### Example 1: set internal-trusted-ca
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c79b045c-6e2f-9e40-94d2-c86246db6ad4",
  "name": "internal_ca",
  "type": "internal-trusted-ca",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1703406766221,
      "iso-8601": "2023-12-24T10:32+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1703079755948,
      "iso-8601": "2023-12-20T15:42+0200"
    },
    "creator": "System"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIDITCCAgmgAwIBAgIBATANBgkqhkiG9w0BAQsFADBDMUEwPwYDVQQKEzhqYWd1\nYXItdDM2My10cnVzdGVkLWNhLW1haW4tdGFrZS0yLmNoZWNrcG9pbnQuY29tLnZk\nNWcyaDAeFw0yMzEyMTkxMzM3NDFaFw0zODAxMTkwMzE0MDdaMEMxQTA/BgNVBAoT\nOGphZ3Vhci10MzYzLXRydXN0ZWQtY2EtbWFpbi10YWtlLTIuY2hlY2twb2ludC5j\nb20udmQ1ZzJoMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAtXqXwyyV\nPlFUVxQb+E9rzQi6BDbB3+TeERTnnDew00oNVMdk23gpc5AlhPVwAywmtlF+uySG\n4poHHZ7T6uwo70CRPwxIwPLtOWp/3pfR+zhPfJ5Ngz2uiWFCDd5kYJGGRjgzjCm1\nuTNah9MM1YoR1eQdiZwHk3o21H8gd48sDffiUPGRSTEnD4OIbMplED2MqVbLX8Pw\nu3g9V6c4HJP+25f69oeW+In1Zznaf5xHojI2wpDY2vRTci0uXx/9aItjLFzpQmlU\nYpBcSfFMK9x0Vp4Un4lk9e9eFGJweGxvX7WtBr0J75efwJKuTUh8XPrCw0pq6Rvc\n0AHJTl5ChkhU0QIDAQABoyAwHjAPBgNVHRMBAf8EBTADAQH/MAsGA1UdDwQEAwIB\nhjANBgkqhkiG9w0BAQsFAAOCAQEAtGzyJVap79j28UKFXhkJ3O5Shuj+UpwJ2vr3\nSztqCD8OUzQi+etKd/z/vCgWa9d4ox/BNMCnPA6P35iKMXs6+BHtDb1YiaBJbTt0\nW/W/Vfcw/cGrxDyFVb8mXLyBWJ+Z40cO2qgLmDWuJSCV+i5ja/28m81kZzMUzd1j\n0zbv6RdQoWRpDkr2YTAhfgSjmB4CovrT+RZ0+w/jS1DcGAPevCSq8n/lIQ/yOp9S\nu/P9EEfoj36fkeS459n/iGPb8lGa/FrzQ9B5Z6Im07RfzCgvfRfrHIu4FriWQ5VF\neeTB23YGKhoJbFnmM6/gONuq1JUw+mSIUdJXJAnQ3CphigJJiw==\n-----END CERTIFICATE-----\n",
  "retrieve-crl-from-http-servers": false,
  "retrieve-crl-from-ldap-servers": false,
  "cache-crl": false,
  "crl-cache-timeout": 1440,
  "allow-certificates-from-branches": false,
  "branches": []
}
```
