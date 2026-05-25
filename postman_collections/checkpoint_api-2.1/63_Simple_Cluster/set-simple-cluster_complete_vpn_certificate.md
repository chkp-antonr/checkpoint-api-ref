# set-simple-cluster complete vpn certificate

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
  "vpn-settings": {
    "certificates": {
      "complete": {
        "name": "new_cert",
        "base64-certificate": "MIIDCzCCAfOgAwIBAgIBAjANBgkqhkiG9w0BAQsFADASMRAwDgYDVQQDEwdDTj10ZXN0MB4XDTI0MDIyMjEzMzEwMFoXDTI1MDEyODA5NDgwMFowDzENMAsGA1UEAxMEdGVzdDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBALdibeUqR8PpNghTsun5gunje8e24IpQJKwPGZ7NaN0c3chu1aXYiVm/45zFrCavFRPsLGh01WDCsAP2ryLCZImFnZnGUoTN4GV27vwdfQk449nZpea+pjKBjd1WfI3owPoshWrQ8UURc7jg91p+xYeSZX0dLsRH60QJkLooByBoQqmpkmppUtPhNHVwMqKqdPHhcDtBMH/PRuJuECYwlHjZr+9LkXSNyIw+XbOE2elyG0inouohDaGySmHuklhEGZc+4580RxrpnHYEGFXq6292jIepWOlorxzqn9Ht7g8hyNVycJyLGWeWjrnWj/LHuCxQf0hODuiq8oIUGbR51IkCAwEAAaNvMG0wDAYDVR0TAQH/BAIwADAdBgNVHQ4EFgQUQKXqEC65n0oX8QoTcHTuWrDdJ8kwCwYDVR0PBAQDAgXgMBEGCWCGSAGG+EIBAQQEAwIGQDAeBglghkgBhvhCAQ0EERYPeGNhIGNlcnRpZmljYXRlMA0GCSqGSIb3DQEBCwUAA4IBAQAb6UTttZxIZ8g4o3z1EZq2gprh8IuMQbMw/DmDMm/MrpJQpUufxiHfDLq2b//39RxNx3PjjN7DnYfUnw2XT5kgwUcIkuTqZLGW0DQOQbJ8668m7lst751elYX3hrPtUvymyUbB0nixL3t/aVPH9XxLpu8sCzcs++g6fJB1UWWuDb3ME8TOede3QBl1eCOpxfYGPpBR/0cma1GRXTvPLMPWMIBm/oDHBvFG2qPVgmeX6zZFDx/rvWOsmBEVw6QcWNi2KqKkB0Fr9Te7Om6N0EVgdddCD/Gdr9MXHDHFxW5GMigghw/XeQ4jPeQ6ibi5FW7l1MfIuMB13NHEVCBOT5nM"
      }
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster complete vpn certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-94d9-ea3679371923"
}
```
