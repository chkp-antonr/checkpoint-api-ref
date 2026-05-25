# add-simple-gateway with ips settings

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
  "name": "gw",
  "ip-address": "1.2.3.4",
  "ips": true,
  "ips-settings": {
    "bypass-all-under-load": false,
    "bypass-track-method": "log",
    "top-cpu-consuming-protections": {
      "disable-under-load": true,
      "disable-period": 8
    }
  }
}
```

## Example Responses

### Example 1: add-simple-gateway with ips settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d97e5a68-e232-4c3a-8e66-9d5163b0ed6a",
  "name": "gw",
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
      "posix": 1735473594659,
      "iso-8601": "2024-12-29T13:59+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1735473594659,
      "iso-8601": "2024-12-29T13:59+0200"
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
  "ipv4-address": "1.2.3.4",
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
  "rtm-traffic-report-per-connection": false,
  "rtm-traffic-report": false,
  "rtm-counters-report": true,
  "anti-spam-and-email-security": false,
  "threat-prevention-mode": "custom",
  "ips": true,
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
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "mgmt_172.23.63.168-lielbe"
  ],
  "send-logs-to-server": [
    "mgmt_172.23.63.168-lielbe"
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
      "main-url": "https://1.2.3.4/",
      "ip-address": "1.2.3.4"
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
    "mgmt_172.23.63.168-lielbe"
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
  "ips-settings": {
    "bypass-all-under-load": false,
    "bypass-track-method": "log",
    "top-cpu-consuming-protections": {
      "disable-under-load": true,
      "disable-period": 8
    },
    "activation-mode": "according-to-policy",
    "cpu-usage-low-threshold": 70,
    "cpu-usage-high-threshold": 90,
    "memory-usage-low-threshold": 70,
    "memory-usage-high-threshold": 90,
    "send-threat-cloud-info": true
  },
  "proxy-settings": {
    "use-custom-proxy": false
  }
}
```
