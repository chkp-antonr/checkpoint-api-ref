# show-simple-cluster with custom exported routes

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-simple-cluster`

## Description

Displays a simple cluster with custom exported routes

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1"
}
```

## Example Responses

### Example 1: show-simple-cluster with custom exported routes
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a0e94ed1-104c-47e4-8134-42a3d95fbd1a",
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
      "posix": 1748514126732,
      "iso-8601": "2025-05-29T13:22+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1748513515482,
      "iso-8601": "2025-05-29T13:11+0300"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": true,
    "delete": true,
    "clone": "not_supported"
  },
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/cluster",
  "nat-settings": {
    "auto-rule": false
  },
  "ipv4-address": "172.23.43.194",
  "dynamic-ip": false,
  "version": "R82.10",
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
        "port": 2746
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
        "port": 443
      },
      "visitor-mode-interface": "All IPs"
    },
    "office-mode": {
      "mode": "off"
    },
    "vpn-domain-exclude-external-ip-addresses": false,
    "certificates": [
      {
        "name": "defaultCert",
        "type": "CpmiCertificate",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "distinguished-name": "CN=cluster1 VPN Certificate,O=MGMT_server.checkpoint.com.ynrf8r",
        "certificate-authority": {
          "uid": "5127437c-b3ba-cd4b-ab1f-95f98a54a2b1",
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
          "posix": 1780049638000,
          "iso-8601": "2026-05-29T13:13+0300"
        }
      }
    ],
    "exported-routes": {
      "static-routes": false,
      "custom-routes": true,
      "internal-interfaces": true,
      "custom-routes-object": {
        "uid": "b80d18e3-7bf5-4305-924f-b58745a71e0b",
        "name": "my_network",
        "type": "network",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/network",
        "color": "black",
        "subnet4": "111.11.1.0",
        "subnet-mask": "255.255.255.0",
        "mask-length4": 24
      }
    }
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
  "anti-bot": true,
  "anti-virus": true,
  "threat-emulation": false,
  "threat-extraction": false,
  "zero-phishing": false,
  "identity-awareness": false,
  "data-loss-prevention": false,
  "qos": false,
  "cluster-xl": true,
  "save-logs-locally": false,
  "send-alerts-to-server": [
    "MGMT_server"
  ],
  "send-logs-to-server": [
    "MGMT_server"
  ],
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
    "stop-logging-when-free-disk-space-below": false,
    "stop-logging-when-free-disk-space-below-threshold": 100,
    "reject-connections-when-free-disk-space-below-threshold": false,
    "reserve-for-packet-capture-metrics": "mbytes",
    "reserve-for-packet-capture-threshold": 500,
    "delete-index-files-when-index-size-above-metrics": "mbytes",
    "delete-index-files-when-index-size-above": false,
    "delete-index-files-when-index-size-above-threshold": 100000,
    "delete-index-files-older-than-days": false,
    "delete-index-files-older-than-days-threshold": 14,
    "forward-logs-to-log-server": true,
    "forward-logs-to-log-server-name": "MGMT_server",
    "forward-logs-to-log-server-schedule-name": "Midnight",
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
      "main-url": "https://172.23.43.194/",
      "ip-address": "172.23.43.194"
    },
    "accessibility": {
      "allow-access-from": "RULE_BASE"
    }
  },
  "usercheck-portal-settings": {
    "enabled": true,
    "portal-web-settings": {
      "main-url": "http://172.23.43.194/UserCheck",
      "ip-address": "172.23.43.194"
    },
    "accessibility": {
      "allow-access-from": "INTERNAL_INTERFACES",
      "internal-access-settings": {
        "undefined": false,
        "dmz": false,
        "vpn": true
      }
    }
  },
  "nat-hide-internal-interfaces": false,
  "communication-with-servers-behind-nat": {
    "override-profile": false
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
        "uid": "d369509d-c567-4250-8a36-f25be4b1c528",
        "name": "eth0",
        "ipv4-address": "172.23.43.194",
        "ipv4-network-mask": "255.255.255.0",
        "ipv4-mask-length": 24,
        "ipv6-address": "",
        "topology": "automatic",
        "topology-automatic-calculation": "external",
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
        "uid": "f461dee1-5e43-43b0-8dc7-7900dfb12e1f",
        "name": "eth1",
        "ipv4-address": "192.168.21.94",
        "ipv4-network-mask": "255.255.255.0",
        "ipv4-mask-length": 24,
        "ipv6-address": "",
        "topology": "automatic",
        "topology-automatic-calculation": "internal",
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
      },
      {
        "uid": "9bcf6fc7-67ae-4621-83ee-614242cdde52",
        "name": "eth2",
        "ipv4-address": "",
        "ipv6-address": "",
        "topology": "automatic",
        "topology-automatic-calculation": "internal",
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
        "interface-type": "private"
      }
    ]
  },
  "cluster-members": [
    {
      "uid": "a38c8f9f-4dd6-4f9e-9b77-030dde9bceb2",
      "name": "GWA",
      "sic-state": "communicating",
      "sic-message": "Trust established",
      "sic-name": "CN=GWA,O=MGMT_server.checkpoint.com.ynrf8r",
      "ip-address": "172.23.43.145",
      "interfaces": [
        {
          "uid": "5fcab39c-8cda-4a3f-acd2-5afbb7b030a8",
          "name": "eth0",
          "ipv4-address": "172.23.43.145",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
        },
        {
          "uid": "e13fe935-fac1-4515-9ba6-91ec227c2baa",
          "name": "eth1",
          "ipv4-address": "192.168.21.5",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
        },
        {
          "uid": "72d95779-2c7f-4d2a-b481-1fbd233a9e83",
          "name": "eth2",
          "ipv4-address": "192.168.31.5",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
        }
      ],
      "ipv6-address": "",
      "priority": 1,
      "comments": "",
      "color": "black"
    },
    {
      "uid": "e3fcde83-e015-4a49-88a9-1de1b4ac0365",
      "name": "GWB",
      "sic-state": "communicating",
      "sic-message": "Trust established",
      "sic-name": "CN=GWB,O=MGMT_server.checkpoint.com.ynrf8r",
      "ip-address": "172.23.43.146",
      "interfaces": [
        {
          "uid": "15eb813a-bf43-45d7-a196-cf7e793b8613",
          "name": "eth0",
          "ipv4-address": "172.23.43.146",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
        },
        {
          "uid": "02f3d72a-0068-4b3e-9a5d-2cde3be49a2b",
          "name": "eth1",
          "ipv4-address": "192.168.21.6",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
        },
        {
          "uid": "c4482b72-2a56-46a3-a58f-aae3c807223b",
          "name": "eth2",
          "ipv4-address": "192.168.31.6",
          "ipv4-network-mask": "255.255.255.0",
          "ipv4-mask-length": 24,
          "ipv6-address": ""
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
  "autonomous-system-number": 0,
  "fetch-policy": [
    "MGMT_server"
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
