# add-simple-gateway with identity sharing

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
  "name": "gw",
  "ip-address": "1.2.3.4",
  "identity-awareness": true,
  "identity-awareness-settings": {
    "identity-agent": true,
    "identity-sharing-settings": {
      "share-with-other-gateways": false,
      "receive-from-other-gateways": true,
      "cache-mode": {
        "override-profile": true,
        "value": true
      },
      "cache-mode-duration": {
        "override-profile": true,
        "value": 99
      },
      "receive-from": "IDServerGW"
    },
    "identity-based-enforcement": "on"
  }
}
```

## Example Responses

### Example 1: add-simple-gateway with identity sharing
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "fe9a3751-8b3b-4ba9-a7c9-48a1d91d99a1",
  "name": "gw",
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
      "posix": 1683792679980,
      "iso-8601": "2023-05-11T11:11+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1683792679980,
      "iso-8601": "2023-05-11T11:11+0300"
    },
    "creator": "WEB_API"
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
  "ipv4-address": "1.9.3.9",
  "dynamic-ip": false,
  "version": "R82",
  "os-name": "Gaia",
  "hardware": "Open server",
  "sic-name": "",
  "sic-state": "uninitialized",
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
  "vpn": false,
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
  "anti-spam-and-email-security": false,
  "threat-prevention-mode": "custom",
  "ips": false,
  "anti-bot": false,
  "anti-virus": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "zero-phishing": false,
  "ips-update-policy": "gateway automatic update",
  "identity-awareness": true,
  "data-loss-prevention": false,
  "qos": false,
  "externally-managed": false,
  "hit-count": true,
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "mgmt_172.23.26.39-jaguar_155_global1MGMT"
  ],
  "send-logs-to-server": [
    "mgmt_172.23.26.39-jaguar_155_global1MGMT"
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
    "turn-on-qos-logging": true,
    "distribute-logs-between-all-active-servers": false
  },
  "platform-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "https://1.9.3.9/",
      "ip-address": "1.9.3.9"
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "nat-hide-internal-interfaces": false,
  "fetch-policy": [
    "mgmt_172.23.26.39-jaguar_155_global1MGMT"
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
  },
  "identity-awareness-settings": {
    "remote-access": false,
    "browser-based-authentication": false,
    "identity-agent": true,
    "identity-collector": false,
    "ad-query": false,
    "terminal-servers": false,
    "radius-accounting": false,
    "collecting-identities": false,
    "identity-agent-settings": {
      "agents-interval-keepalive": 5,
      "user-reauthenticate-interval": 480,
      "identity-agent-portal-settings": {
        "portal-web-settings": {
          "main-url": "https://0.0.0.0/_IAAgent",
          "ip-address": "0.0.0.0"
        },
        "accessibility": {
          "allow-access-from": "INTERNAL_INTERFACES",
          "internal-access-settings": {
            "undefined": false,
            "dmz": false,
            "vpn": false
          }
        }
      },
      "authentication-settings": {
        "authentication-method": "defined_on_user",
        "users-directories": {
          "internal-users": false,
          "external-user-profile": false,
          "users-from-external-directories": "all gateways directories"
        }
      }
    },
    "identity-sharing-settings": {
      "share-with-other-gateways": false,
      "receive-from-other-gateways": true,
      "cache-mode": {
        "override-profile": true,
        "profile-value": true,
        "value": true
      },
      "cache-mode-duration": {
        "override-profile": true,
        "profile-value": 60,
        "value": 99
      },
      "receive-from": [
        {
          "uid": "e141f65f-ba7e-40cd-913c-fb9e08b56504",
          "name": "IDServerGW",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        }
      ]
    },
    "proxy-settings": {
      "detect-using-x-forward-for": false
    },
    "identity-based-enforcement": "on",
    "identity-web-api": false
  },
  "proxy-settings": {
    "use-custom-proxy": false
  }
}
```
