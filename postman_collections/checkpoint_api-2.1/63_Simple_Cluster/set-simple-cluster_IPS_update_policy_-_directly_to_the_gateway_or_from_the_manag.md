# set-simple-cluster IPS update policy - directly to the gateway or from the management

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
  "ips-update-policy": "via management"
}
```

## Example Responses

### Example 1: set-simple-cluster IPS update policy - directly to the gateway or from the management
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a4763059-b254-4394-a4d4-d61a026a8bf2",
  "name": "cluster1",
  "type": "simple-cluster",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1644402204598,
      "iso-8601": "2022-02-09T12:23+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1644402124510,
      "iso-8601": "2022-02-09T12:22+0200"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/cluster",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "1.2.2.4",
  "dynamic-ip": false,
  "version": "R81.20",
  "os-name": "Gaia",
  "hardware": "Open server",
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
  "application-control": false,
  "url-filtering": false,
  "application-control-and-url-filtering-settings": {
    "global-settings-mode": "use_global_settings"
  },
  "content-awareness": false,
  "threat-prevention-mode": "custom",
  "ips": false,
  "anti-bot": false,
  "anti-virus": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "zero-phishing": false,
  "identity-awareness": false,
  "data-loss-prevention": false,
  "qos": false,
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "ivory-main-take-310"
  ],
  "send-logs-to-server": [
    "ivory-main-take-310"
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
  "hit-count": true,
  "platform-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "https://1.2.2.4/",
      "ip-address": "1.2.2.4",
      "aliases": []
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "nat-hide-internal-interfaces": false,
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
  "cluster-mode": "cluster-xl-ha",
  "geo-mode": false,
  "ips-update-policy": "gateway automatic update",
  "fetch-policy": [
    "ivory-main-take-310"
  ],
  "cluster-settings": {
    "track-changes-of-cluster-members": "log",
    "state-synchronization": {
      "enabled": true,
      "delayed": true,
      "delayed-seconds": 3
    },
    "use-virtual-mac": false,
    "member-recovery-mode": "maintain-current-active"
  },
  "proxy-settings": {
    "use-custom-proxy": false
  }
}
```
