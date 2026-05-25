# set-simple-gateway renew vpn certificate

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

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
  "vpn-settings": {
    "certificates": {
      "renew": {
        "name": "defaultCert",
        "alternate-names": [
          {
            "name-type": "ip address",
            "value": "2.2.2.2"
          },
          {
            "name-type": "email",
            "value": "new_email"
          }
        ]
      }
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway renew vpn certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d01f057f-2e2c-4f9b-914d-63d32acf6642",
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
      "posix": 1708608929048,
      "iso-8601": "2024-02-22T15:35+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1708608029407,
      "iso-8601": "2024-02-22T15:20+0200"
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
    "authentication": {},
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
        "status": "signed",
        "stored-at": "management server",
        "expiration-date": {
          "posix": 1738057680000,
          "iso-8601": "2025-01-28T11:48+0200"
        },
        "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIDCzCCAfOgAwIBAgIBAjANBgkqhkiG9w0BAQsFADASMRAwDgYDVQQDEwdDTj10\r\nZXN0MB4XDTI0MDIyMjEzMzEwMFoXDTI1MDEyODA5NDgwMFowDzENMAsGA1UEAxME\r\ndGVzdDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBALdibeUqR8PpNghT\r\nsun5gunje8e24IpQJKwPGZ7NaN0c3chu1aXYiVm/45zFrCavFRPsLGh01WDCsAP2\r\nryLCZImFnZnGUoTN4GV27vwdfQk449nZpea+pjKBjd1WfI3owPoshWrQ8UURc7jg\r\n91p+xYeSZX0dLsRH60QJkLooByBoQqmpkmppUtPhNHVwMqKqdPHhcDtBMH/PRuJu\r\nECYwlHjZr+9LkXSNyIw+XbOE2elyG0inouohDaGySmHuklhEGZc+4580RxrpnHYE\r\nGFXq6292jIepWOlorxzqn9Ht7g8hyNVycJyLGWeWjrnWj/LHuCxQf0hODuiq8oIU\r\nGbR51IkCAwEAAaNvMG0wDAYDVR0TAQH/BAIwADAdBgNVHQ4EFgQUQKXqEC65n0oX\r\n8QoTcHTuWrDdJ8kwCwYDVR0PBAQDAgXgMBEGCWCGSAGG+EIBAQQEAwIGQDAeBglg\r\nhkgBhvhCAQ0EERYPeGNhIGNlcnRpZmljYXRlMA0GCSqGSIb3DQEBCwUAA4IBAQAb\r\n6UTttZxIZ8g4o3z1EZq2gprh8IuMQbMw/DmDMm/MrpJQpUufxiHfDLq2b//39RxN\r\nx3PjjN7DnYfUnw2XT5kgwUcIkuTqZLGW0DQOQbJ8668m7lst751elYX3hrPtUvym\r\nyUbB0nixL3t/aVPH9XxLpu8sCzcs++g6fJB1UWWuDb3ME8TOede3QBl1eCOpxfYG\r\nPpBR/0cma1GRXTvPLMPWMIBm/oDHBvFG2qPVgmeX6zZFDx/rvWOsmBEVw6QcWNi2\r\nKqKkB0Fr9Te7Om6N0EVgdddCD/Gdr9MXHDHFxW5GMigghw/XeQ4jPeQ6ibi5FW7l\r\n1MfIuMB13NHEVCBOT5nM\r\n-----END CERTIFICATE-----\n"
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
          "posix": 1740144927000,
          "iso-8601": "2025-02-21T15:35+0200"
        },
        "base64-certificate": "-----BEGIN CERTIFICATE-----\nMIIEHTCCAwWgAwIBAgIDAI4GMA0GCSqGSIb3DQEBCwUAMEMxQTA/BgNVBAoTOGph\r\nZ3Vhci10NTExLXRydXN0ZWQtY2EtbWFpbi10YWtlLTMuY2hlY2twb2ludC5jb20u\r\nODc3dGR2MB4XDTI0MDIyMTEzMzUyN1oXDTI1MDIyMTEzMzUyN1owYTFBMD8GA1UE\r\nChM4amFndWFyLXQ1MTEtdHJ1c3RlZC1jYS1tYWluLXRha2UtMy5jaGVja3BvaW50\r\nLmNvbS44Nzd0ZHYxHDAaBgNVBAMTE2d3MSBWUE4gQ2VydGlmaWNhdGUwggEiMA0G\r\nCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCgdUv+jyEjUZ2aNqclXILSTGLB2f9g\r\nHJ8yf94CZ/envGsUHwUDrDsCZ66XfzI8S9YJ+N3XoeUlLOP81gCY13jbP4F/dAMO\r\n7u6anPalo1sBcLxaOaD7OtbD4eRIRjF/QqgqR6r23T74eUYvbH3pDOMSWEorXl5A\r\nj3BFjX97G7WBtpUyzTy96g3IoIpcIqJ8y5VErFSSYB0KmqzVjrSkuSOw8wd1+3jF\r\nlbE7TVM2zpqzAv377DMD/Beu4lcTPfGw9YFyDgFJeWu85/v6PqMtbsDaGWKhertQ\r\nfF4Ml6iSuxsiLdaeqaNwrYBGa45SnJsjo+IL+arXGAyJ9CHih6ijLXEFAgMBAAGj\r\ngfswgfgwgawGA1UdHwSBpDCBoTCBnqCBm6CBmIY8aHR0cDovL2phZ3Vhci10NTEx\r\nLXRydXN0ZWQtY2EtbWFpbi10YWtlLTM6MTgyNjQvSUNBX0NSTDEuY3JspFgwVjFB\r\nMD8GA1UEChM4amFndWFyLXQ1MTEtdHJ1c3RlZC1jYS1tYWluLXRha2UtMy5jaGVj\r\na3BvaW50LmNvbS44Nzd0ZHYxETAPBgNVBAMMCElDQV9DUkwxMAkGA1UdEwQCMAAw\r\nGgYDVR0RBBMwEYcEAgICAoEJbmV3X2VtYWlsMAsGA1UdDwQEAwIFoDATBgNVHSUE\r\nDDAKBggrBgEFBQcDATANBgkqhkiG9w0BAQsFAAOCAQEAsfdct/B0KtB5qP7MMYEO\r\n9EvScekjYvQw7FjKvQOtVP3eOM1DuUbD7IlIC628ZWvrEw8iw7eqpmrfwzZT7T9J\r\nXuTFQ57rQi1qK3qV10E8ZIFcJbxDsQplkV+ZpISwynsIwwPxDy7nMfyuRtebLogS\r\nG69nRqTQn8yMxd4ChzDK47Oo48jNmwKhpdge5FTgPfSAEb2jbEGpteDM1gTFv2/x\r\nrhTccLHj5PeS0t5DLNe1+D7HaCpj9KFtI1Witssi4g8SYOqEiOZTCucy8AIrsVOP\r\nkTti7pWUchrKDZZ5WxDOsa6e1hxYcIo+I92FQX4SVbB/P91VRfcI3r6ruxGYf5oP\r\nEA==\r\n-----END CERTIFICATE-----\n"
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
      "ip-address": "1.1.1.1",
      "aliases": []
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
    "outbound-certificate": {
      "override-profile": false,
      "profile-value": ""
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
