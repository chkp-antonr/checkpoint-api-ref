# show-simple-gateway (Enhanced Link Selection Interfaces)

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-simple-gateway`

## Description

Displays a gateway with enhanced link selection interfaces

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Gateway_2_version_R82.10"
}
```

## Example Responses

### Example 1: show-simple-gateway (Enhanced Link Selection Interfaces)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "cc693ce4-9a7d-496b-b530-9461b50b9179",
  "name": "Gateway_2_version_R82.10",
  "type": "simple-gateway",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1703496865108,
      "iso-8601": "2023-12-25T11:34+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1703496848896,
      "iso-8601": "2023-12-25T11:34+0200"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "not_supported"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/gateway",
  "groups": [],
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "172.23.42.151",
  "dynamic-ip": false,
  "version": "R82",
  "os-name": "Gaia",
  "hardware": "Open server",
  "interfaces": [
    {
      "uid": "d557db72-803a-4521-844f-3724b48502ad",
      "name": "eth0",
      "ipv4-address": "172.23.42.151",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": "",
      "topology": "external",
      "anti-spoofing": false,
      "security-zone": false,
      "comments": "",
      "color": "black",
      "icon": "NetworkObjects/network",
      "network-interface-type": "ethernet"
    },
    {
      "uid": "879ea3a5-b439-4ec3-a2de-c7125c39fda0",
      "name": "eth1",
      "ipv4-address": "10.20.30.41",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": "",
      "topology": "internal",
      "topology-settings": {
        "ip-address-behind-this-interface": "not defined",
        "interface-leads-to-dmz": false
      },
      "anti-spoofing": false,
      "security-zone": false,
      "comments": "",
      "color": "black",
      "icon": "NetworkObjects/network",
      "network-interface-type": "ethernet"
    },
    {
      "uid": "6f9c899d-94a0-4163-b618-64f0bae4d04d",
      "name": "eth2",
      "ipv4-address": "172.43.52.201",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": "fe81::1234",
      "ipv6-network-mask": "ffff:ffff:ffff:ffff:ffff::",
      "ipv6-mask-length": 80,
      "topology": "external",
      "anti-spoofing": false,
      "security-zone": false,
      "comments": "",
      "color": "black",
      "icon": "NetworkObjects/network",
      "network-interface-type": "ethernet"
    },
    {
      "uid": "085dbabd-5321-464f-b2ac-257710f3b30e",
      "name": "eth3",
      "ipv4-address": "172.23.43.151",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": "",
      "topology": "external",
      "anti-spoofing": false,
      "security-zone": false,
      "comments": "",
      "color": "black",
      "icon": "NetworkObjects/network",
      "network-interface-type": "ethernet"
    }
  ],
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
    "maximum-concurrent-ike-negotiations": 1000,
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1702833041075,
            "iso-8601": "2023-12-17T19:10+0200"
          },
          "last-modifier": "System",
          "creation-time": {
            "posix": 1702833041075,
            "iso-8601": "2023-12-17T19:10+0200"
          },
          "creator": "System"
        },
        "available-actions": {
          "edit": "false",
          "delete": "false",
          "clone": "true"
        },
        "tags": [],
        "read-only": true,
        "comments": "Check Point VPN-1 SecuRemote IPSEC Transport Encapsulation Protocol",
        "color": "firebrick",
        "icon": "Services/UDPService",
        "groups": [
          "97aeb475-9aea-11d5-bd16-0090272ccb30"
        ],
        "keep-connections-open-after-policy-installation": false,
        "session-timeout": 40,
        "use-default-session-timeout": true,
        "match-for-any": true,
        "sync-connections-on-cluster": true,
        "aggressive-aging": {
          "enable": true,
          "timeout": 15,
          "use-default-timeout": true,
          "default-timeout": 0
        },
        "override-default-settings": false,
        "port": "2746",
        "match-by-protocol-signature": false,
        "accept-replies": true
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
        "meta-info": {
          "lock": "unlocked",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1702833044160,
            "iso-8601": "2023-12-17T19:10+0200"
          },
          "last-modifier": "System",
          "creation-time": {
            "posix": 1702833044160,
            "iso-8601": "2023-12-17T19:10+0200"
          },
          "creator": "System"
        },
        "available-actions": {
          "edit": "false",
          "delete": "false",
          "clone": "true"
        },
        "tags": [],
        "read-only": true,
        "comments": "HTTP protocol over TLS/SSL",
        "color": "red",
        "icon": "Services/TCPService",
        "groups": [
          "82bccbc2-603c-4d96-a59b-9c2b730efb5c",
          "7f9275f0-4382-4222-b4cd-06d2c5aa3222"
        ],
        "keep-connections-open-after-policy-installation": false,
        "session-timeout": 3600,
        "use-default-session-timeout": true,
        "match-for-any": true,
        "sync-connections-on-cluster": true,
        "aggressive-aging": {
          "enable": true,
          "timeout": 60,
          "use-default-timeout": false,
          "default-timeout": 60
        },
        "override-default-settings": false,
        "port": "443",
        "protocol": "ENC-HTTP",
        "match-by-protocol-signature": false,
        "enable-tcp-resource": false,
        "use-delayed-sync": false,
        "delayed-sync-value": 30
      },
      "visitor-mode-interface": "All IPs"
    },
    "office-mode": {
      "mode": "off"
    },
    "vpn-domain-exclude-external-ip-addresses": false,
    "authentication": {},
    "interfaces": [
      {
        "interface-name": "eth2",
        "next-hop-ip": "172.43.52.100",
        "static-nat-ip": "10.20.30.10",
        "redundancy-mode": "active",
        "ip-version": "ipv4"
      },
      {
        "interface-name": "eth0",
        "next-hop-ip": "172.23.42.100",
        "static-nat-ip": "50.40.30.10",
        "priority": 7,
        "redundancy-mode": "backup",
        "ip-version": "ipv4"
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
    "jaguar-tpi-t393-main-take-5"
  ],
  "send-logs-to-server": [
    "jaguar-tpi-t393-main-take-5"
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
      "main-url": "https://172.23.42.151/",
      "ip-address": "172.23.42.151",
      "aliases": []
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "nat-hide-internal-interfaces": false,
  "fetch-policy": [
    "jaguar-tpi-t393-main-take-5"
  ],
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
  "platform": "open server",
  "auto-topology-use-custom-recalculation-time": false,
  "auto-topology-custom-recalculation-time": 10,
  "autonomous-system-number": "0",
  "proxy-settings": {
    "use-custom-proxy": false
  }
}
```
