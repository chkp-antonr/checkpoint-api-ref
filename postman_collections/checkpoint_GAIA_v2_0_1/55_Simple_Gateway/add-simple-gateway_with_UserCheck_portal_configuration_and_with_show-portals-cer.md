# add-simple-gateway with UserCheck portal configuration and with show-portals-certificate flag

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
  "ipv4-address": "1.1.1.1",
  "application-control": true,
  "usercheck-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "aliases": [
        "www.blabla1.com"
      ]
    },
    "certificate-settings": {
      "base64-certificate": "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",
      "base64-password": "YmFkc3NsLmNvbQ=="
    },
    "accessibility": {
      "allow-access-from": "INTERNAL_INTERFACES",
      "internal-access-settings": {
        "undefined": true,
        "dmz": true,
        "vpn": true
      }
    }
  },
  "show-portals-certificate": true
}
```

## Example Responses

### Example 1: add-simple-gateway with UserCheck portal configuration and with show-portals-certificate flag
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "42d0a54c-5fc0-471f-80f2-295cc3266967",
  "name": "gw1",
  "type": "simple-gateway",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1605800886308,
      "iso-8601": "2020-11-19T17:48+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1605800883907,
      "iso-8601": "2020-11-19T17:48+0200"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "ipv4-address": "1.1.1.1",
  "dynamic-ip": false,
  "version": "R81",
  "os-name": "Gaia",
  "hardware": "Open server",
  "sic-name": "",
  "sic-state": "uninitialized",
  "interfaces": [],
  "firewall": true,
  "firewall-settings": {
    "auto-maximum-limit-for-concurrent-connections": true,
    "maximum-limit-for-concurrent-connections": 25000,
    "auto-calculate-connections-hash-table-size-and-memory-pool": true,
    "connections-hash-size": 131072,
    "memory-pool-size": 6,
    "maximum-memory-pool-size": 30
  },
  "vpn": false,
  "application-control": true,
  "url-filtering": false,
  "content-awareness": false,
  "ips": false,
  "anti-bot": false,
  "anti-virus": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "identity-awareness": false,
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "ice-t392-mp-api-main-take-13"
  ],
  "send-logs-to-server": [
    "ice-t392-mp-api-main-take-13"
  ],
  "send-logs-to-backup-server": [],
  "logs-settings": {
    "rotate-log-by-file-size": false,
    "rotate-log-file-size-threshold": 1000,
    "rotate-log-on-schedule": false,
    "alert-when-free-disk-space-below-metrics": "mbytes",
    "alert-when-free-disk-space-below": true,
    "alert-when-free-disk-space-below-threshold": 20,
    "alert-when-free-disk-space-below-type": "popup alert",
    "delete-when-free-disk-space-below-metrics": "mbytes",
    "delete-when-free-disk-space-below": true,
    "delete-when-free-disk-space-below-threshold": 5000,
    "before-delete-keep-logs-from-the-last-days": false,
    "before-delete-keep-logs-from-the-last-days-threshold": 3664,
    "before-delete-run-script": false,
    "before-delete-run-script-command": "",
    "stop-logging-when-free-disk-space-below-metrics": "mbytes",
    "stop-logging-when-free-disk-space-below": true,
    "stop-logging-when-free-disk-space-below-threshold": 100,
    "reject-connections-when-free-disk-space-below-threshold": false,
    "reserve-for-packet-capture-metrics": "mbytes",
    "reserve-for-packet-capture-threshold": 500,
    "delete-index-files-when-index-size-above-metrics": "mbytes",
    "delete-index-files-when-index-size-above": false,
    "delete-index-files-when-index-size-above-threshold": 100000,
    "delete-index-files-older-than-days": false,
    "delete-index-files-older-than-days-threshold": 14,
    "forward-logs-to-log-server": false,
    "perform-log-rotate-before-log-forwarding": false,
    "update-account-log-every": 3600,
    "detect-new-citrix-ica-application-names": false,
    "turn-on-qos-logging": true
  },
  "platform-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "https://1.1.1.1/",
      "ip-address": "1.1.1.1"
    },
    "certificate-settings": {
      "certificate-valid-from": "16-Nov-17",
      "certificate-valid-to": "16-Nov-19",
      "certificate-dn": "CN=BadSSL Client Certificate,O=BadSSL,L=San Francisco,ST=California,C=US",
      "certificate": "-----BEGIN CERTIFICATE-----MIIEnTCCAoWgAwIBAgIJAPC7KMFjfslXMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlhMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMQ8wDQYDVQQKDAZCYWRTU0wxMTAvBgNVBAMMKEJhZFNTTCBDbGllbnQgUm9vdCBDZXJ0aWZpY2F0ZSBBdXRob3JpdHkwHhcNMTcxMTE2MDUzNjMzWhcNMTkxMTE2MDUzNjMzWjBvMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEPMA0GA1UECgwGQmFkU1NMMSIwIAYDVQQDDBlCYWRTU0wgQ2xpZW50IENlcnRpZmljYXRlMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxzdfEeseTs/rukjly6MSLHM+Rh0enA3Ai4Mj2sdl31x3SbPoen08utVhjPmlxIUdkiMG4+ffe7N+JtDLG75CaxZp9CxytX7kywooRBJsRnQhmQPca8MRWAJBIz+w/L+3AFkTIqWBfyT+1VO8TVKPkEpGdLDovZOmzZAASi9/sj+j6gM7AaCiDeZTf2ES66abA5pOp60Q6OEdwg/vCUJfarhKDpi9tj3P6qToy9Y4DiBUhOct4MG8w5XwmKAC+Vfm8tb7tMiUoU0yvKKOcL6YXBXxB2kPcOYxYNobXavfVBEdwSrjQ7i/s3o6hkGQlm9F7JPEuVgbl/Jdwa64OYIqjQIDAQABoy0wKzAJBgNVHRMEAjAAMBEGCWCGSAGG+EIBAQQEAwIHgDALBgNVHQ8EBAMCBeAwDQYJKoZIhvcNAQELBQADggIBAKpzk1ZTunWuof3DIer2Abq7IV3STGeFaoH4TuHdSbmXwC0KuPkv7wVPgPekyRaHb9CBnsreRF7eleD1M63kakhdnA1XIbdJw8sfSDlKdI4emmb4fzdaaPxbrkQ5IxOBQDw5rTUFVPPqFWw1bGP2zrKD1/i1pxUtGM0xem1jR7UZYpsSPs0JCOHKZOmk8OEWUy+Jp4gRzbMLZ0TrvajGEZXRepjOkXObR81xZGtvTNP2wl1zm13ffwIYdqJUrf1HH4miU9lVX+3/Z+2mVHBWhzBgbTmo06s3uwUE6JsxUGm2/w4NNblRit0uQcGw7ba8kl2d5rZQscFsqNFz2vRjj1G0dO8S3owmuF0izZO9Fqvq0jB6oaUkxcAcTKFSjs2zwy1oy+cu8iO3GRbfAW7U0xzGp9MnkdPS5dHzvhod3/DK0YVskfxZF7M8GhkjT7Qm2EUBQNNMNXC3g/GXTdXOgqqjW5GXahI8Z6Q4OYN6xZwuEhizwKkgojwaww2YgYT9MJXciJZWr3QXvFdBH7m0zwpKgQ1wm6j3yeyuRphq2lEtU3OQl55A3tXtvqyMXsxkxMCCNQdmKQt0WYmMS3Xj/AfAY2sjCWziDflvW5mGCUjSYdZ+r3JIIF4m/FNCIO1dIoacp9qb0qL9duFlVHtFiPgoKrEdJaNVUL7NG9ppF8pR-----END CERTIFICATE-----"
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "usercheck-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "http://1.1.1.1/UserCheck",
      "ip-address": "1.1.1.1",
      "aliases": [
        "www.blabla1.com"
      ]
    },
    "certificate-settings": {
      "certificate-valid-from": "16-Nov-17",
      "certificate-valid-to": "16-Nov-19",
      "certificate-dn": "CN=BadSSL Client Certificate,O=BadSSL,L=San Francisco,ST=California,C=US",
      "certificate": "-----BEGIN CERTIFICATE-----MIIEnTCCAoWgAwIBAgIJAPC7KMFjfslXMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlhMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMQ8wDQYDVQQKDAZCYWRTU0wxMTAvBgNVBAMMKEJhZFNTTCBDbGllbnQgUm9vdCBDZXJ0aWZpY2F0ZSBBdXRob3JpdHkwHhcNMTcxMTE2MDUzNjMzWhcNMTkxMTE2MDUzNjMzWjBvMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEPMA0GA1UECgwGQmFkU1NMMSIwIAYDVQQDDBlCYWRTU0wgQ2xpZW50IENlcnRpZmljYXRlMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxzdfEeseTs/rukjly6MSLHM+Rh0enA3Ai4Mj2sdl31x3SbPoen08utVhjPmlxIUdkiMG4+ffe7N+JtDLG75CaxZp9CxytX7kywooRBJsRnQhmQPca8MRWAJBIz+w/L+3AFkTIqWBfyT+1VO8TVKPkEpGdLDovZOmzZAASi9/sj+j6gM7AaCiDeZTf2ES66abA5pOp60Q6OEdwg/vCUJfarhKDpi9tj3P6qToy9Y4DiBUhOct4MG8w5XwmKAC+Vfm8tb7tMiUoU0yvKKOcL6YXBXxB2kPcOYxYNobXavfVBEdwSrjQ7i/s3o6hkGQlm9F7JPEuVgbl/Jdwa64OYIqjQIDAQABoy0wKzAJBgNVHRMEAjAAMBEGCWCGSAGG+EIBAQQEAwIHgDALBgNVHQ8EBAMCBeAwDQYJKoZIhvcNAQELBQADggIBAKpzk1ZTunWuof3DIer2Abq7IV3STGeFaoH4TuHdSbmXwC0KuPkv7wVPgPekyRaHb9CBnsreRF7eleD1M63kakhdnA1XIbdJw8sfSDlKdI4emmb4fzdaaPxbrkQ5IxOBQDw5rTUFVPPqFWw1bGP2zrKD1/i1pxUtGM0xem1jR7UZYpsSPs0JCOHKZOmk8OEWUy+Jp4gRzbMLZ0TrvajGEZXRepjOkXObR81xZGtvTNP2wl1zm13ffwIYdqJUrf1HH4miU9lVX+3/Z+2mVHBWhzBgbTmo06s3uwUE6JsxUGm2/w4NNblRit0uQcGw7ba8kl2d5rZQscFsqNFz2vRjj1G0dO8S3owmuF0izZO9Fqvq0jB6oaUkxcAcTKFSjs2zwy1oy+cu8iO3GRbfAW7U0xzGp9MnkdPS5dHzvhod3/DK0YVskfxZF7M8GhkjT7Qm2EUBQNNMNXC3g/GXTdXOgqqjW5GXahI8Z6Q4OYN6xZwuEhizwKkgojwaww2YgYT9MJXciJZWr3QXvFdBH7m0zwpKgQ1wm6j3yeyuRphq2lEtU3OQl55A3tXtvqyMXsxkxMCCNQdmKQt0WYmMS3Xj/AfAY2sjCWziDflvW5mGCUjSYdZ+r3JIIF4m/FNCIO1dIoacp9qb0qL9duFlVHtFiPgoKrEdJaNVUL7NG9ppF8pR-----END CERTIFICATE-----"
    },
    "accessibility": {
      "allow-access-from": "INTERNAL_INTERFACES",
      "internal-access-settings": {
        "undefined": true,
        "dmz": true,
        "vpn": true
      }
    }
  },
  "enable-https-inspection": false,
  "https-inspection": {
    "bypass-on-failure": {
      "override-profile": false,
      "profile-value": true
    },
    "site-categorization-allow-mode": {
      "override-profile": false,
      "profile-value": "hold"
    },
    "deny-untrusted-server-cert": {
      "override-profile": false,
      "profile-value": false
    },
    "deny-expired-server-cert": {
      "override-profile": false,
      "profile-value": false
    },
    "outbound-certificate": {
      "override-profile": false,
      "profile-value": {
        "uid": "f215045c-a773-45c2-8f71-0ff3e25c3b2d",
        "name": "OutboundCertificate",
        "type": "outbound-inspection-certificate",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "subject_user_certificate",
        "color": "black"
      }
    },
    "deny-revoked-server-cert": {
      "override-profile": false,
      "profile-value": true
    }
  }
}
```
