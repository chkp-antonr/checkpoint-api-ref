# set-cp-trusted-ca-certificate

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-cp-trusted-ca-certificate`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "c7253c5f-5881-4d4a-b82b-f111b2182403",
  "status": "disabled"
}
```

## Example Responses

### Example 1: set-cp-trusted-ca-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c7253c5f-5881-4d4a-b82b-f111b2182403",
  "name": "CA_0090EA36_7A7C_42DF_93EE_CFE97D542FFB",
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
      "posix": 1690179340137,
      "iso-8601": "2023-07-24T09:15+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1690179340137,
      "iso-8601": "2023-07-24T09:15+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "issued-to": "CN=GeoTrust Universal CA 2, O=GeoTrust Inc., C=US",
  "issued-by": "CN=GeoTrust Universal CA 2, O=GeoTrust Inc., C=US",
  "valid-from": {
    "posix": 1678665600000,
    "iso-8601": "2023-03-13T02:00+0200"
  },
  "valid-to": {
    "posix": 1686527999000,
    "iso-8601": "2023-06-12T02:59+0300"
  },
  "added-by": "Check Point",
  "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIFbDCCA1SgAwIBAgIBATANBgkqhkiG9w0BAQUFADBHMQswCQYDVQQGEwJVUzEWMBQGA1UEChMNR2VvVHJ1c3QgSW5jLjEgMB4GA1UEAxMXR2VvVHJ1c3QgVW5pdmVyc2FsIENBIDIwHhcNMDQwMzA0MDUwMDAwWhcNMjkwMzA0MDUwMDAwWjBHMQswCQYDVQQGEwJVUzEWMBQGA1UEChMNR2VvVHJ1c3QgSW5jLjEgMB4GA1UEAxMXR2VvVHJ1c3QgVW5pdmVyc2FsIENBIDIwggIiMA0GCSqGSIb3DQEBAQUAA4ICDwAwggIKAoICAQCzVFLByT7y2dyxUxpZKeexw0Uo5dfR7cXFS6GqdHtXr0om/Nj1XqduGdt0DE81WzILAePb63p3NeqqWuDW6KFXlPCQo3RWlEQwAx5cTiuFJnSCegx2oG9NzkEtoBUGFF+3Qs17j1hhNNwqCPkuwwGmIkQcTAeC5lvO0Ep8BNMZcyfwqph/Lq9O64ceJHdqXbboW0W63MOhBW9Wjo8QJqVJwy7XQYci4E+GymC16qFjwAGXEHm9ADwSbSsVsaxLse4YuU6W3Nx2/zu+z18DwPw76L5GG//aQMJS9/7jOvdqdzXQ2o3rXhhqMcceujwbKNZrVMaqW9eiLBsZzKIC9ptZvTdrhrVtgrrY6slWvKk2WP0+GfPtDCapkzj4T8FdIgbQl+rhrcZV4IErKIM6+vR7IVEAvlI4zs1meaj0gVbi0IMJR1FbUGrP20gaXT73y/Zl92zxlfgCOzJWgjl6W70viRu/obTo/3+NjN8D8WBOWBFM66M/ECuDmgFz2ZRthAAnZqzwcEAJQpKtT5MNYQlRJNiS1QuUYbKHsu3/mjX/hVTK7URDrBs8FmtISgocQIgfksILAAX/8sgCSqSqqcyZlpwvWOB94b67B9xfBHJcMTTD7F8t4D1kkCLm0ey4Lt1ZrtmhN79UNdxzMk+MBB4zsslG8dhcyFVQyWi9qLo2CQIDAQABo2MwYTAPBgNVHRMBAf8EBTADAQH/MB0GA1UdDgQWBBR281Xh+qQ2+/CfXGJx7Tz0RzgQKzAfBgNVHSMEGDAWgBR281Xh+qQ2+/CfXGJx7Tz0RzgQKzAOBgNVHQ8BAf8EBAMCAYYwDQYJKoZIhvcNAQEFBQADggIBAGbBxiPz2eAubl/oz66wsCVNK/g7WJtAJDday6sWSf+zdXkzoS9tcBc0kf5nfo/sm+VegqlVHy/c1FEHEv6sFj4sNcZj/NwQ6w2jqtB8zNHQL1EuxBRa3ugZ4T7GzKQp5y6EqgYweHZUcyiYWTjgAA1i00J9IZ+uPTqM1fp3DRgrFg5fNuH8KrUwJM/gYwx7WBr+mbpCErGR9Hxo4sjoryzqyX6uuyo9DRXcNJW2GHSoag/HtPQTxORb7QrSpJdMKu0vbBKJPfEncKpqA1Ihn0CoZ1Dy81of398j9tx4TuaYT1U6U+Pv8vSfx3zYWK8pIpe44L2RLrB27FcRz+8pRPPphXpgY+RdM4kX2TGq2tbzGDVyz4crL2MjhF2EjD9XoIj8mZEoJmmZ1I+XRL6O1UixpCgp8RW04eWe3fiPpm8m1wk8OhwRDqZsN/etRIcsKMfYdIKz0G9KV7s1KSegi+ghp4dkNl3M2Basx7InQJJVOCiNUW7dFGdTbHFcJoRNdVq2fmBWqU2t+5sel/MN2dKXVHfaPRK34B7vCAas+YWH6aLcr34YEoP9VhdBLtUpgn2Z9DH2canPLAEnpQW5qrJITirvn5NSUZU8UnOOVkwXQMAJKOSLakhT2+zNVVXxxvjpoixMptEmX36vWkzaH6byHCx+rgIW0lbQL1dTR+iS\r\n-----END CERTIFICATE-----\n",
  "status": "disabled"
}
```
