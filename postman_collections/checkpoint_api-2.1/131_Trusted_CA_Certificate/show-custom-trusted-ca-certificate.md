# show-custom-trusted-ca-certificate

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-custom-trusted-ca-certificate`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "f6afaa0f-f978-4b1c-8575-6cbc9459af11"
}
```

## Example Responses

### Example 1: show-custom-trusted-ca-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f6afaa0f-f978-4b1c-8575-6cbc9459af11",
  "name": "CA_F6AFAA0F_F978_4B1C_8575_6CBC9459AF11",
  "type": "custom-trusted-ca-certificate",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1699196133630,
      "iso-8601": "2023-11-05T16:55+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1699196133630,
      "iso-8601": "2023-11-05T16:55+0200"
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
  "issued-to": "CN=*.whatsapp.net, O='Meta Platforms, Inc.', L=Menlo Park, ST=California, C=US",
  "issued-by": "E=il_security@checkpoint.com, CN=CheckPoint-SSL-Inspection, OU=MIS, O=CheckPoint Software Technologies LTD., ST=Israel, C=IL",
  "valid-from": {
    "posix": 1678665600000,
    "iso-8601": "2023-03-13T02:00+0200"
  },
  "valid-to": {
    "posix": 1686527999000,
    "iso-8601": "2023-06-12T02:59+0300"
  },
  "added-by": "User",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIEkzCCAnugAwIBAgIVAO5SRZQELwNNhWF+8st6ox9uXYgeMA0GCSqGSIb3DQEBCwUAMIGrMQswCQYDVQQGEwJJTDEPMA0GA1UECBMGSXNyYWVsMS4wLAYDVQQKEyVDaGVja1BvaW50IFNvZnR3YXJlIFRlY2hub2xvZ2llcyBMVEQuMQwwCgYDVQQLEwNNSVMxIjAgBgNVBAMTGUNoZWNrUG9pbnQtU1NMLUluc3BlY3Rpb24xKTAnBgkqhkiG9w0BCQEWGmlsX3NlY3VyaXR5QGNoZWNrcG9pbnQuY29tMB4XDTIzMDMxMzAwMDAwMFoXDTIzMDYxMTIzNTk1OVowbzELMAkGA1UEBhMCVVMxEzARBgNVBAgTCkNhbGlmb3JuaWExEzARBgNVBAcTCk1lbmxvIFBhcmsxHTAbBgNVBAoTFE1ldGEgUGxhdGZvcm1zLCBJbmMuMRcwFQYDVQQDDA4qLndoYXRzYXBwLm5ldDBZMBMGByqGSM49AgEGCCqGSM49AwEHA0IABPjo05vRHAJYYWx55SOu2b1ZIQPOOtJNipSBXf1BFBDQhrkp20YTA296MzKii2j3TgVi/1t44cW5mD1RWobfAQujgbMwgbAwHQYDVR0lBBYwFAYIKwYBBQUHAwEGCCsGAQUFBwMCMHQGA1UdEQRtMGuCDioud2hhdHNhcHAubmV0ghIqLmNkbi53aGF0c2FwcC5uZXSCEiouc25yLndoYXRzYXBwLm5ldIIOKi53aGF0c2FwcC5jb22CBXdhLm1lggx3aGF0c2FwcC5jb22CDHdoYXRzYXBwLm5ldDAOBgNVHQ8BAf8EBAMCBaAwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAgEAA/sIadLr9ahEVq8h9HuofHODUuzxVFulAZu8uSiyY4ACbaHcvm36MYQCzYV56t4fe+I++ls8KAESZgdE0KoD5/6efzK05Ufok+y15QexAR5AxZlJqtoHIuc7iOolPbkLW77GKrbgfEgmwOCX9/86Pug4ZSrrBUPPt9i3accNkAP+SH9Lft1geS2E/q+xcRhbhDcYTYD56X0MiEv0UaAzwS3adWAZbD7R42u+xNCpX8iUyiwp2UvMf0l/+Q8CAtw4D5s/8hD7Vqvrv4H/ZfV7SrZ+rPrihi01t6LlcpZ2YMucX/tSgDzkjYWmT26V2OgRklM0aQWvHD3DVpghIJfI2swAAJJ5wvqwcJeAWHAQb3aQZgHXjGF/LyBYCQsohTHUL7rhL8CxNlDTNhN2e+NRFGYGer157RCmM8xKroe3/X9pYifbzyEWInqQ+ycmLsQyAd7pPW+W1K1tlk9Niqk3dNQ10daYGau3IPWF5+iHtOlWjLcQrSj60Uv7Ebi0E+bOe0tDabunCj6SEauGFxeJhM9xUZnOwb5wqIt+uGqPQ9WRJLehqwdFhiWOqwUfNcksn7l0M6e9Mnkh1J2kGxamQ0bvK7ftpm5O8MTAft0y882IfC++Zuk4gLhQoeE3s6877/rrHRJB/H8ZUaaBxAi2qH0NZ+ParXUxOkil5rVgFqI=\r\n-----END CERTIFICATE-----\n"
}
```
