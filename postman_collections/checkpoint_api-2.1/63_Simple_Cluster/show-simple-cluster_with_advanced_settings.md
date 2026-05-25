# show-simple-cluster with advanced settings

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-simple-cluster`

## Description

Displays a cluster with advances settings

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
  "show-advanced-settings": "true"
}
```

## Example Responses

### Example 1: show-simple-cluster with advanced settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c01518e0-928f-42c9-9c9a-311edd74baa5",
  "name": "cluster1",
  "type": "simple-cluster",
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
      "posix": 1734962813613,
      "iso-8601": "2024-12-23T16:06+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734962771347,
      "iso-8601": "2024-12-23T16:06+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "not_supported"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "yellow",
  "icon": "NetworkObjects/cluster",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "17.23.5.1",
  "dynamic-ip": false,
  "version": "R82",
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
  "identity-awareness": false,
  "data-loss-prevention": false,
  "qos": false,
  "cluster-xl": true,
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "MGMT"
  ],
  "send-logs-to-server": [
    "MGMT"
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
      "main-url": "https://17.23.5.1/",
      "ip-address": "17.23.5.1",
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
  "rtm-traffic-report-per-connection": false,
  "rtm-traffic-report": false,
  "rtm-counters-report": true,
  "interfaces": {
    "total": 3,
    "from": 1,
    "to": 3,
    "objects": [
      {
        "uid": "88da916c-6320-4c53-bc44-331211fe018a",
        "name": "eth0",
        "ipv4-address": "17.23.5.1",
        "ipv4-network-mask": "255.255.255.0",
        "ipv4-mask-length": 24,
        "ipv6-address": "",
        "topology": "external",
        "anti-spoofing": true,
        "anti-spoofing-settings": {
          "action": "prevent",
          "exclude-packets": false,
          "spoof-tracking": "log"
        },
        "security-zone": false,
        "comments": "",
        "color": "black",
        "icon": "NetworkObjects/network",
        "network-interface-type": "ethernet",
        "interface-type": "cluster"
      },
      {
        "uid": "4b2b69fa-1e90-4a7a-aec5-b19d0f4f653f",
        "name": "eth1",
        "ipv4-address": "1.1.2.0",
        "ipv4-network-mask": "255.255.255.0",
        "ipv4-mask-length": 24,
        "ipv6-address": "",
        "topology": "internal",
        "topology-settings": {
          "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
          "interface-leads-to-dmz": false
        },
        "anti-spoofing": false,
        "security-zone": false,
        "comments": "",
        "color": "black",
        "icon": "NetworkObjects/network",
        "network-interface-type": "ethernet",
        "interface-type": "sync"
      },
      {
        "uid": "ed0d90d5-cbf6-48c0-9b1d-e254a8fa8155",
        "name": "eth2",
        "ipv4-address": "192.168.1.1",
        "ipv4-network-mask": "255.255.255.0",
        "ipv4-mask-length": 24,
        "ipv6-address": "",
        "topology": "internal",
        "topology-settings": {
          "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
          "interface-leads-to-dmz": false
        },
        "anti-spoofing": true,
        "anti-spoofing-settings": {
          "action": "prevent",
          "exclude-packets": false,
          "spoof-tracking": "log"
        },
        "security-zone": false,
        "comments": "",
        "color": "black",
        "icon": "NetworkObjects/network",
        "network-interface-type": "ethernet",
        "interface-type": "cluster"
      }
    ]
  },
  "cluster-members": [
    {
      "uid": "9e16a9a3-7af5-457e-a70d-fba636d0146a",
      "name": "member1",
      "sic-state": "initialized",
      "trust-state": "initialized",
      "sic-message": "Initialized but trust not established",
      "sic-name": "",
      "ip-address": "17.23.5.2",
      "interfaces": [
        {
          "uid": "9d48bf89-5f84-470d-9dcf-6338c025106c",
          "name": "eth0",
          "ipv4-address": "17.23.5.2",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        },
        {
          "uid": "3a74ff90-5e1f-4c6a-bc4c-932abeee5055",
          "name": "eth1",
          "ipv4-address": "1.1.2.4",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        },
        {
          "uid": "12636906-73f2-420c-abae-13f19db3351c",
          "name": "eth2",
          "ipv4-address": "192.168.1.2",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        }
      ],
      "ipv6-address": "",
      "priority": 1,
      "comments": "",
      "color": "black"
    },
    {
      "uid": "5abaca2d-4a0a-4a91-9897-db7d249b1ce9",
      "name": "member2",
      "sic-state": "initialized",
      "trust-state": "initialized",
      "sic-message": "Initialized but trust not established",
      "sic-name": "",
      "ip-address": "17.23.5.3",
      "interfaces": [
        {
          "uid": "022ab379-cc47-430f-a903-06d019539137",
          "name": "eth0",
          "ipv4-address": "17.23.5.3",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        },
        {
          "uid": "153d6157-cffd-4a73-a80c-084b5139194f",
          "name": "eth1",
          "ipv4-address": "1.1.2.5",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        },
        {
          "uid": "0421d7c6-0b98-438d-973d-fe534a9321cd",
          "name": "eth2",
          "ipv4-address": "192.168.1.3",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": "",
          "ipv6-network-mask": "::",
          "ipv6-mask-length": 0
        }
      ],
      "ipv6-address": "",
      "priority": 2,
      "comments": "",
      "color": "black"
    }
  ],
  "cluster-mode": "cluster-xl-ha",
  "geo-mode": false,
  "ips-update-policy": "gateway automatic update",
  "autonomous-system-number": "0",
  "fetch-policy": [
    "MGMT"
  ],
  "auto-topology-use-custom-recalculation-time": false,
  "auto-topology-custom-recalculation-time": 10,
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
