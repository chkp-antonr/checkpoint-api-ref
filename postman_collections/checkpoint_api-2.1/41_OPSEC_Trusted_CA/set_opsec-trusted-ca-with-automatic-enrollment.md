# set opsec-trusted-ca-with-automatic-enrollment

**Collection:** Web API (version 2.1) > 41 OPSEC Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-opsec-trusted-ca`

## Description

Set opsec trusted ca with automatic enrollment

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "opsec_ca",
  "automatic-enrollment": {
    "automatically-enroll-certificate": "true",
    "protocol": "cmpv1",
    "cmpv1-settings": {
      "direct-tcp-settings": {
        "ip-address": "1.1.1.1"
      }
    }
  }
}
```

## Example Responses

### Example 1: set opsec-trusted-ca-with-automatic-enrollment
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
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1703590970954,
      "iso-8601": "2023-12-26T13:42+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1703590631273,
      "iso-8601": "2023-12-26T13:37+0200"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/account_unit",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIICwjCCAaqgAwIBAgIIVBWw0wYzja0wDQYJKoZIhvcNAQELBQAwGDEWMBQGA1UE\nAxMNd3d3Lm9wc2VjLmNvbTAeFw0yMzExMjEwOTE2MDBaFw0yNDExMjAxNjAwMDBa\nMBgxFjAUBgNVBAMTDXd3dy5vcHNlYy5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IB\nDwAwggEKAoIBAQCjpqCxDaVg+I1b+wqnmjjYtL3v7Tlu/YpMbsKnv+M1gRz6QFUO\noSVnxKLo0A7Y4kCqa1OPcHO/LtXuok43F1YZPVKm3xWpY8FmqGqf5ZuGmSwm1HPO\nbcMjwGOyFgwpwEDF5e0UMZ7xtJF8BZ5KKBh3ZfQ1FbmbVqSUPcmOi+NE4JspPlHx\nX+m6es/yeSGR1A2ezKY7KePTlwVtDe8hiLrYyKG92nka5rkD1QyEIVJ0W5wrnU4n\nGEDIHeOfT09zroQxaNLkb51sl4Tog/qw+EraVGIBe/iFnSJoDF37i2mLJqI/t8be\nl+aGDAxgMx1pO85OClgjPSWL0UIXGI2xrR+JAgMBAAGjEDAOMAwGA1UdEwQFMAMB\nAf8wDQYJKoZIhvcNAQELBQADggEBAFU2bL1lBTSx9F4o1J2oTZRA4DRghmUTq72P\nLWmC6hXUXJTJunz4JuNLxeW0s1ATbQxVJ9qRuWBNY3J9vl61sgPDLvwGhJ4zuNIy\n8M3y0lZi7q1iy5eKrmtKx9gwE9jcSjw2hNk7R5E+0046hwYKEWdUdtzdvUdUvRoZ\nGy8l6psrQkNLvwWIohtqixeXKPnuWocRAryTUlYTGcUctIQ3c2IKvPDFodAjdFwT\n5Q4gmkzze0Q5gLw66YMMJuQZ+Z0EkqMSCSjkb6bqqlfMRtKh/C+iRxXqXn2RnknD\njD+BDF0oT4UKWyYETZ+HGUm3Q5n6Flg6RH4UDcxp9C3Y5VpkOtA=\n-----END CERTIFICATE-----\n",
  "retrieve-crl-from-http-servers": true,
  "retrieve-crl-from-ldap-servers": false,
  "cache-crl": true,
  "crl-cache-method": "timeout",
  "crl-cache-timeout": 1440,
  "allow-certificates-from-branches": false,
  "branches": [],
  "automatic-enrollment": {
    "automatically-enroll-certificate": true,
    "protocol": "cmpv1",
    "cmpv1-settings": {
      "transport-layer": "direct-tcp",
      "direct-tcp-settings": {
        "ip-address": "1.1.1.1",
        "port": 829
      }
    }
  }
}
```
