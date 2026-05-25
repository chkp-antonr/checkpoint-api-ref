# show opsec-trusted-ca

**Collection:** Web API (version 2.1) > 41 OPSEC Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-opsec-trusted-ca`

## Description

Show opsec trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "opsec_ca"
}
```

## Example Responses

### Example 1: show opsec-trusted-ca
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "24dfc6a6-a0a3-4d12-90e5-295d9790f3b9",
  "name": "opsec_ca",
  "type": "opsec-trusted-ca",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1703170011352,
      "iso-8601": "2023-12-21T16:46+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1703170011352,
      "iso-8601": "2023-12-21T16:46+0200"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIICwjCCAaqgAwIBAgIILdexblpVEMIwDQYJKoZIhvcNAQELBQAwGDEWMBQGA1UE\nAxMNd3d3Lm9wc2VjLmNvbTAeFw0yMzA2MjUwOTE3MDBaFw0yNTAzMzExNjAwMDBa\nMBgxFjAUBgNVBAMTDXd3dy5vcHNlYy5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IB\nDwAwggEKAoIBAQCjpqCxDaVg+I1b+wqnmjjYtL3v7Tlu/YpMbsKnv+M1gRz6QFUO\noSVnxKLo0A7Y4kCqa1OPcHO/LtXuok43F1YZPVKm3xWpY8FmqGqf5ZuGmSwm1HPO\nbcMjwGOyFgwpwEDF5e0UMZ7xtJF8BZ5KKBh3ZfQ1FbmbVqSUPcmOi+NE4JspPlHx\nX+m6es/yeSGR1A2ezKY7KePTlwVtDe8hiLrYyKG92nka5rkD1QyEIVJ0W5wrnU4n\nGEDIHeOfT09zroQxaNLkb51sl4Tog/qw+EraVGIBe/iFnSJoDF37i2mLJqI/t8be\nl+aGDAxgMx1pO85OClgjPSWL0UIXGI2xrR+JAgMBAAGjEDAOMAwGA1UdEwQFMAMB\nAf8wDQYJKoZIhvcNAQELBQADggEBAHTs1AutAmSLHF2KRLJtrRNkso0lMyA7XI7k\n1TNpTk7TCZLNY0VbUliGbcl+POH4EG8ARUrftnwRDCTBd2BdJTqG2CyNADi+bw8a\nLvbxok7KH0GlQvGjyfq+sHK12wTl4ULNyYoAPZ01GhXOvkobROdSyjxvBVhxdVo9\n0kj7mHFv3N83huNhfstDFUBcQCmMkbLuzDUZrl2a1OtqlOdNC6mNvb7Jq9W9vRxG\nA514e7jqyoM+PwHu5fILx/jmGT8suOUnvbtcDdFhjqixAPer6uSPR0CSbiJvuDy7\n2DPH5mjZK5dQKewNYOZ/BQEsRIBe+Q6eGAoJqi+cD63cwlw0DCc=\n-----END CERTIFICATE-----\n",
  "retrieve-crl-from-http-servers": true,
  "retrieve-crl-from-ldap-servers": false,
  "cache-crl": true,
  "crl-cache-method": "timeout",
  "crl-cache-timeout": 1440,
  "allow-certificates-from-branches": false,
  "branches": [],
  "automatic-enrollment": {
    "automatically-enroll-certificate": false
  }
}
```
