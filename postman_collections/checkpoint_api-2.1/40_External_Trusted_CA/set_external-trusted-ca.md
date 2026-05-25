# set external-trusted-ca

**Collection:** Web API (version 2.1) > 40 External Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-external-trusted-ca`

## Description

Set external trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "external_ca",
  "base64-certificate": "MIICujCCAaKgAwIBAgIIFbLYzT2+3TMwDQYJKoZIhvcNAQELBQAwFDESMBAGA1UEAxMJd3d3LnouY29tMB4XDTI0MDIwMTEyMzEwMFoXDTI0MTIzMTE2MDAwMFowFDESMBAGA1UEAxMJd3d3LnouY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAoBreRGuq8u43GBog+ZaAnaR8ZF8cT2ppvtd3JoFmzTOQivLIt9sNtFYqEgHCtnNkKn9TRrxN14YscHgKIxfDSVlC9Rh0rrBvWgFqcm715Whr99Ogx6JbYFkusFWJarSejIFx4n6MM48MJxLdtCP6Hy1G2cj1BCiCHj4i3VIVaDE/aMkSqJbYEvf+vFqUWxY8/uEuKI/HGhI7mhUPW4NSGL0Oafz5eEFVsxqV5NA19/JJZ9NajSkyANnaNL5raxGV0oeqaE3JB3lSEZfWbH6mQsToUxxwIQfsZiIBozajDdTgP3Kn4SMY0b+I/WAWgfigMSDTAIR8J1sdzGXy2w2kqQIDAQABoxAwDjAMBgNVHRMEBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQBxaE9O/LCjKfWeugPeDPvr3Ld0i1mYsgNIyN+ES1iDoJHXrBQpVzZelJRr8leFgbghGUX7Fwdh1qZ2Jw6nmD1oe/Q7jkPzTngb6dIMI/kFK4eXcS4GJ3S7yGobLB7QUKK1vrYWZdNuAzR6jMRmFECS+lPF7zlTexnwwOkATMp6lzS7xEpEhk/8eLpSQnYzvsM+rL9voU5q9MrdAJ2XaCZe4Crv75NdYU6ljD2eSYDrO148Tg480TlvT5wzBuyanKhI/Po2oLEVWU7h5tkensHKB5zvxigIr9ZkczdzVbbrRFi2jSQy+VxYWc0zCo/uO+yaKmmLfGDQEb8wZYY1Ml27",
  "retrieve-crl-from-http-servers": "false",
  "crl-cache-method": "expiration date"
}
```

## Example Responses

### Example 1: set external-trusted-ca
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
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIICujCCAaKgAwIBAgIIFbLYzT2+3TMwDQYJKoZIhvcNAQELBQAwFDESMBAGA1UE\nAxMJd3d3LnouY29tMB4XDTI0MDIwMTEyMzEwMFoXDTI0MTIzMTE2MDAwMFowFDES\nMBAGA1UEAxMJd3d3LnouY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKC\nAQEAoBreRGuq8u43GBog+ZaAnaR8ZF8cT2ppvtd3JoFmzTOQivLIt9sNtFYqEgHC\ntnNkKn9TRrxN14YscHgKIxfDSVlC9Rh0rrBvWgFqcm715Whr99Ogx6JbYFkusFWJ\narSejIFx4n6MM48MJxLdtCP6Hy1G2cj1BCiCHj4i3VIVaDE/aMkSqJbYEvf+vFqU\nWxY8/uEuKI/HGhI7mhUPW4NSGL0Oafz5eEFVsxqV5NA19/JJZ9NajSkyANnaNL5r\naxGV0oeqaE3JB3lSEZfWbH6mQsToUxxwIQfsZiIBozajDdTgP3Kn4SMY0b+I/WAW\ngfigMSDTAIR8J1sdzGXy2w2kqQIDAQABoxAwDjAMBgNVHRMEBTADAQH/MA0GCSqG\nSIb3DQEBCwUAA4IBAQBxaE9O/LCjKfWeugPeDPvr3Ld0i1mYsgNIyN+ES1iDoJHX\nrBQpVzZelJRr8leFgbghGUX7Fwdh1qZ2Jw6nmD1oe/Q7jkPzTngb6dIMI/kFK4eX\ncS4GJ3S7yGobLB7QUKK1vrYWZdNuAzR6jMRmFECS+lPF7zlTexnwwOkATMp6lzS7\nxEpEhk/8eLpSQnYzvsM+rL9voU5q9MrdAJ2XaCZe4Crv75NdYU6ljD2eSYDrO148\nTg480TlvT5wzBuyanKhI/Po2oLEVWU7h5tkensHKB5zvxigIr9ZkczdzVbbrRFi2\njSQy+VxYWc0zCo/uO+yaKmmLfGDQEb8wZYY1Ml27\n-----END CERTIFICATE-----\n",
  "retrieve-crl-from-http-servers": false,
  "retrieve-crl-from-ldap-servers": false,
  "cache-crl": true,
  "crl-cache-method": "expiration date",
  "crl-cache-timeout": 1440,
  "allow-certificates-from-branches": false,
  "branches": []
}
```
