# add-simple-gateway with vpn certificate

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-simple-gateway`

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
  "ip-address": "1.1.1.1",
  "vpn-settings": {
    "certificates": {
      "name": "new_cert",
      "certificate-authority": "trusted_ca",
      "enrollment": {
        "enrollment-settings": {
          "distinguished-name": "CN=test"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: add-simple-gateway with vpn certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "212b5cf1-be85-483a-8eed-cfcddbac9c94",
  "name": "gw1",
  "type": "simple-gateway",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "platform": "open server",
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1708605674325,
      "iso-8601": "2024-02-22T14:41+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1708605674325,
      "iso-8601": "2024-02-22T14:41+0200"
    },
    "creator": "aa"
  },
  "available-actions": {
    "clone": "not_supported"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "1.1.1.1",
  "dynamic-ip": false,
  "version": "R82",
  "os-name": "Gaia",
  "hardware": "Open server",
  "interfaces": [],
  "network-policy-management": false,
  "log-server": false,
  "firewall": true,
  "firewall-settings": {
    "auto-maximum-limit-for-concurrent-connections": true,
    "maximum-limit-for-concurrent-connections": 25000,
    "auto-calculate-connections-hash-table-size-and-memory-pool": true,
    "connections-hash-size": 131072,
    "memory-pool-size": 6,
    "maximum-memory-pool-size": 30
  },
  "vpn": true,
  "vpn-settings": {
    "useClientlessVpn": false,
    "maximum-concurrent-ike-negotiations": 10000,
    "maximum-concurrent-tunnels": 10000,
    "vpn-domain-type": "addresses_behind_gw",
    "link-selection": {
      "ip-selection": "use-main-address"
    },
    "remote-access": {
      "support-l2tp": false,
      "allow-vpn-clients-to-route-traffic": false,
      "support-nat-traversal-mechanism": true,
      "nat-traversal-service": {
        "uid": "97aeb390-9aea-11d5-bd16-0090272ccb30",
        "name": "VPN1_IPSEC_encapsulation",
        "type": "service-udp",
        "domain": {
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data",
          "domain-type": "data domain"
        },
        "icon": "Services/UDPService",
        "color": "firebrick",
        "port": "2746"
      },
      "support-visitor-mode": true,
      "visitor-mode-service": {
        "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30",
        "name": "https",
        "type": "service-tcp",
        "domain": {
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data",
          "domain-type": "data domain"
        },
        "icon": "Protocols/HTTP",
        "color": "red",
        "port": "443"
      },
      "visitor-mode-interface": "All IPs"
    },
    "office-mode": {
      "mode": "off"
    },
    "vpn-domain-exclude-external-ip-addresses": false,
    "interfaces": [],
    "certificates": [
      {
        "name": "new_cert",
        "type": "CpmiCertificate",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "distinguished-name": "CN=test",
        "certificate-authority": {
          "uid": "c311ebd0-dbe9-4e84-b26b-85e7a1913e08",
          "name": "trusted_ca",
          "type": "opsec-trusted-ca",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "Objects/account_unit",
          "color": "black"
        },
        "status": "unsigned",
        "stored-at": "management server",
        "base64-certificate": "-----BEGIN CERTIFICATE REQUEST-----\nMIICcjCCAVoCAQAwDzENMAsGA1UEAxMEdGVzdDCCASIwDQYJKoZIhvcNAQEBBQAD\r\nggEPADCCAQoCggEBAKRDabAQDL6vAeX3zQqOQBdaMZEn06pxY5yx2B6shCYXdc8F\r\nITkaTGFxNCimin1A+lW0AB5pIh+aVsBW4PCmU0sklzMnS2NudznKc27Zpwq9OK9c\r\nuUCw6rmRyTv5otdViP2lmfP50PPA8+b3lefHbXecwKSJ8l9MH/sl+XYViaYRVJUO\r\n1oFOh0mT9f/of0gx8PjbnFVGIxStZEcY/gqhETk7EV3msd+6CLhPKbDt8wq6IIPo\r\nF9yHc9T6EGWN7KEgxFik/9ObiAPUrqr37muVya5p7kLALwRSWcjOgmxXlbf1fQX1\r\nko40iDkmjpKKJx0NkXg+5Z2Ddz0JYk5Oo/hhhUUCAwEAAaAeMBwGCSqGSIb3DQEJ\r\nDjEPMA0wCwYDVR0PBAQDAgWgMA0GCSqGSIb3DQEBCwUAA4IBAQAVZeLbsILDoDrF\r\nW9yOc7uO5nQcwENBENU+u6PaeL7KPkCQCrZ4zV2f1WggZsQwBrN73Dw/bOaN1iuN\r\nzXUC6l2imsPeKH1ZO0fbgNPNNOiGYdJgSKmRW/Q3KcxPOvR3tHXHYsCBYE88oRLR\r\ncCUNQ/nLhkWQu8tc7kS65ynnxaYous8pusq0KpQC8BEzfpQQKlW2D7OFZLczKUeY\r\nhwm6F149Pl5+jvSJKOTeFOvEB02LFCv6Xd+W+kFwVrpIVZeOQ1vEB4qxnsqM8CjY\r\n40VO+peaLu0bsIxjkea9u2bmz+pPtIbXgIU+gXaQ8vi1X4Ikh8usiSJl1gxf0eak\r\nu2N/1PvR\r\n-----END CERTIFICATE REQUEST-----"
      },
      {
        "name": "defaultCert",
        "type": "CpmiCertificate",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "distinguished-name": "CN=gw1 VPN Certificate,O=jaguar-t511-trusted-ca-main-take-3.checkpoint.com.877tdv",
        "certificate-authority": {
          "uid": "3fbbc166-4e00-7645-b802-0746485b6692",
          "name": "internal_ca",
          "type": "internal-trusted-ca",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "Objects/account_unit",
          "color": "black"
        },
        "status": "signed",
        "stored-at": "management server",
        "expiration-date": {
          "posix": 1740141673000,
          "iso-8601": "2025-02-21T14:41+0200"
        },
        "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIEETCCAvmgAwIBAgICNBUwDQYJKoZIhvcNAQELBQAwQzFBMD8GA1UEChM4amFn\r\ndWFyLXQ1MTEtdHJ1c3RlZC1jYS1tYWluLXRha2UtMy5jaGVja3BvaW50LmNvbS44\r\nNzd0ZHYwHhcNMjQwMjIxMTI0MTEzWhcNMjUwMjIxMTI0MTEzWjBhMUEwPwYDVQQK\r\nEzhqYWd1YXItdDUxMS10cnVzdGVkLWNhLW1haW4tdGFrZS0zLmNoZWNrcG9pbnQu\r\nY29tLjg3N3RkdjEcMBoGA1UEAxMTZ3cxIFZQTiBDZXJ0aWZpY2F0ZTCCASIwDQYJ\r\nKoZIhvcNAQEBBQADggEPADCCAQoCggEBAL4svb8NPa9iVNhnS83oKhVRRGG8A053\r\niySmmGDIWJl3seMZnmJEehvkpPMlf00kbj7KyzKTyRjnKAJW9Jp35thU4P/5yQ9f\r\n7DvOtEC5coHmDb+Th7BnqFcVIvCfM/05GwdN4QvZ2WxmlAYV6x6rUnyA94EDrg8S\r\nAr1tcKMLjsXfeyRYBSyEqoT9wbc5gxKvKA1FmHngWLE8ApvytvtcJ7KbABKYwLas\r\nzOQODkGqkIGZ/lfraysZdfmsMaSg0PdIQbNVqv6QfIvkDU0BVDiv9xBbBbBBaKyz\r\n2Vjvc5RFS0k5nGIznTTV6rwKR7drMEC0nDWF7XeNshpPim868QUfvdUCAwEAAaOB\r\n8DCB7TCBrAYDVR0fBIGkMIGhMIGeoIGboIGYhjxodHRwOi8vamFndWFyLXQ1MTEt\r\ndHJ1c3RlZC1jYS1tYWluLXRha2UtMzoxODI2NC9JQ0FfQ1JMMS5jcmykWDBWMUEw\r\nPwYDVQQKEzhqYWd1YXItdDUxMS10cnVzdGVkLWNhLW1haW4tdGFrZS0zLmNoZWNr\r\ncG9pbnQuY29tLjg3N3RkdjERMA8GA1UEAwwISUNBX0NSTDEwCQYDVR0TBAIwADAP\r\nBgNVHREECDAGhwQBAQEBMAsGA1UdDwQEAwIFoDATBgNVHSUEDDAKBggrBgEFBQcD\r\nATANBgkqhkiG9w0BAQsFAAOCAQEAly5nG6O9KoyChj7F+EsSywm4jwl0dcPAUrmt\r\nmM0uSQI9k72J2y72OUf4ZQgEsbLFJ63AOSFBXylBDrzLE0gWd8xGHyPdoLGcjTgK\r\nZf7cLIszkz25nRJLxiFFEdr3vf4a7eiWr5a7+bI7GqwwJbnkukv8HjNF0nBUgPeX\r\nLAVqiWQqIVoKVJYuEEaTk+BY7SMT/Y9LgPvQDbhdNIgC8xc4S7/s+Mzlmp97hWTY\r\nhsXBM3cP3por0ZHyeBI/LYDgJuC8MmcX/DkKkWucNmdaCZY3ep/O9ji/dzVtdufD\r\nerP5FBCy6G6Jk/lB+EaYkULlE4ubxPHVOylE1sN0rlrsWJrlMg==\r\n-----END CERTIFICATE-----\n"
      }
    ]
  },
  "policy-server": false,
  "mobile-access": false,
  "application-control": false,
  "url-filtering": false,
  "legacy-url-filtering": false,
  "application-control-and-url-filtering-settings": {
    "global-settings-mode": "use_global_settings"
  },
  "content-awareness": false,
  "monitoring": false,
  "rtm-traffic-report-per-connection": false,
  "rtm-traffic-report": false,
  "rtm-counters-report": true,
  "anti-spam-and-email-security": false,
  "threat-prevention-mode": "custom",
  "ips": false,
  "anti-bot": false,
  "anti-virus": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "zero-phishing": false,
  "ips-update-policy": "gateway automatic update",
  "identity-awareness": false,
  "data-loss-prevention": false,
  "qos": false,
  "externally-managed": false,
  "hit-count": true,
  "sic-name": "",
  "sic-state": "uninitialized",
  "trust-state": "uninitialized",
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "jaguar-t511-trusted-ca-main-take-3"
  ],
  "send-logs-to-server": [
    "jaguar-t511-trusted-ca-main-take-3"
  ],
  "send-logs-to-backup-server": [],
  "logs-settings": {
    "rotate-log-by-file-size": false,
    "rotate-log-file-size-threshold": 1000,
    "rotate-log-on-schedule": false,
    "alert-when-free-disk-space-below-metrics": "mbytes",
    "alert-when-free-disk-space-below": true,
    "alert-when-free-disk-space-below-threshold": 3000,
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
    "turn-on-qos-logging": true,
    "distribute-logs-between-all-active-servers": false
  },
  "platform-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "https://1.1.1.1/",
      "ip-address": "1.1.1.1"
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "nat-hide-internal-interfaces": false,
  "communication-with-servers-behind-nat": {
    "override-profile": false
  },
  "fetch-policy": [
    "jaguar-t511-trusted-ca-main-take-3"
  ],
  "advanced-settings": {
    "sam": {
      "forward-to-other-sam-servers": false,
      "purge-sam-file": {
        "enabled": false,
        "purge-when-size-reaches-to": 100
      },
      "use-early-versions": {
        "enabled": false
      }
    },
    "connection-persistence": "rematch-connections"
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
    "bypass-on-client-failure": {
      "override-profile": false,
      "profile-value": true
    },
    "bypass-under-load": {
      "value": false
    },
    "deployment-mode": "full",
    "deny-revoked-server-cert": {
      "override-profile": false,
      "profile-value": true
    }
  },
  "zero-phishing-settings": {
    "gateway-fqdn-mode": "automatic"
  },
  "auto-topology-use-custom-recalculation-time": false,
  "auto-topology-custom-recalculation-time": 10,
  "proxy-settings": {
    "use-custom-proxy": false
  }
}
```
