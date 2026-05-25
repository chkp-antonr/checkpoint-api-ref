# show subordinate-cas

**Collection:** Web API (version 2.1) > 45 Subordinate CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-subordinate-cas`

## Description

Show all subordinate CA.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5,
  "offset": 0,
  "details-level": "full"
}
```

## Example Responses

### Example 1: show subordinate-cas
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "44c0ae26-6335-4059-81c2-47b59149ca8f",
      "name": "TestSubordinateCa",
      "type": "subordinate-ca",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1751541861108,
          "iso-8601": "2025-07-03T14:24+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1751541428240,
          "iso-8601": "2025-07-03T14:17+0300"
        },
        "creator": "WEB_API"
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
      "automatic-enrollment": {
        "automatically-enroll-certificate": true,
        "protocol": "cmpv1",
        "cmpv1-settings": {
          "direct-tcp-settings": {
            "ip-address": "1.1.1.1",
            "port": 829
          }
        }
      },
      "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIICwjCCAaqgAwIBAgIILdexblpVEMIwDQYJKoZIhvcNAQELBQAwGDEWMBQGA1UE\nAxMNd3d3Lm9wc2VjLmNvbTAeFw0yMzA2MjUwOTE3MDBaFw0yNTAzMzExNjAwMDBa\nMBgxFjAUBgNVBAMTDXd3dy5vcHNlYy5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IB\nDwAwggEKAoIBAQCjpqCxDaVg+I1b+wqnmjjYtL3v7Tlu/YpMbsKnv+M1gRz6QFUO\noSVnxKLo0A7Y4kCqa1OPcHO/LtXuok43F1YZPVKm3xWpY8FmqGqf5ZuGmSwm1HPO\nbcMjwGOyFgwpwEDF5e0UMZ7xtJF8BZ5KKBh3ZfQ1FbmbVqSUPcmOi+NE4JspPlHx\nX+m6es/yeSGR1A2ezKY7KePTlwVtDe8hiLrYyKG92nka5rkD1QyEIVJ0W5wrnU4n\nGEDIHeOfT09zroQxaNLkb51sl4Tog/qw+EraVGIBe/iFnSJoDF37i2mLJqI/t8be\nl+aGDAxgMx1pO85OClgjPSWL0UIXGI2xrR+JAgMBAAGjEDAOMAwGA1UdEwQFMAMB\nAf8wDQYJKoZIhvcNAQELBQADggEBAHTs1AutAmSLHF2KRLJtrRNkso0lMyA7XI7k\n1TNpTk7TCZLNY0VbUliGbcl+POH4EG8ARUrftnwRDCTBd2BdJTqG2CyNADi+bw8a\nLvbxok7KH0GlQvGjyfq+sHK12wTl4ULNyYoAPZ01GhXOvkobROdSyjxvBVhxdVo9\n0kj7mHFv3N83huNhfstDFUBcQCmMkbLuzDUZrl2a1OtqlOdNC6mNvb7Jq9W9vRxG\nA514e7jqyoM+PwHu5fILx/jmGT8suOUnvbtcDdFhjqixAPer6uSPR0CSbiJvuDy7\n2DPH5mjZK5dQKewNYOZ/BQEsRIBe+Q6eGAoJqi+cD63cwlw0DCc=\n-----END CERTIFICATE-----\n"
    }
  ]
}
```
