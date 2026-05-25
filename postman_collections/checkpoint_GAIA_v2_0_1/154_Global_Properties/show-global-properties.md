# show-global-properties

**Collection:** Web API (version 2.0.1) > 154 Global Properties
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-global-properties`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-global-properties
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "309f47b2-f6d5-488d-9d82-14d07aba9ade",
  "name": "firewall_properties",
  "type": "global-properties",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1683618773623,
      "iso-8601": "2023-05-09T10:52+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1683444454860,
      "iso-8601": "2023-05-07T10:27+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "read-only": false,
  "icon": "General/settings",
  "firewall": {
    "accept-control-connections": true,
    "accept-control-connections-position": "first",
    "accept-remote-access-control-connections": true,
    "accept-remote-access-control-connections-position": "first",
    "accept-smart-update-connections": true,
    "accept-smart-update-connections-position": "first",
    "accept-ips1-management-connections": true,
    "accept-ips1-management-connections-position": "first",
    "accept-outgoing-packets-originating-from-gw": true,
    "accept-outgoing-packets-originating-from-gw-position": "before last",
    "accept-outgoing-packets-originating-from-connectra-gw": true,
    "accept-outgoing-packets-to-cp-online-services": true,
    "accept-outgoing-packets-to-cp-online-services-position": "before last",
    "accept-rip": false,
    "accept-rip-position": "first",
    "accept-domain-name-over-udp": false,
    "accept-domain-name-over-udp-position": "first",
    "accept-domain-name-over-tcp": false,
    "accept-domain-name-over-tcp-position": "first",
    "accept-icmp-requests": false,
    "accept-icmp-requests-position": "before last",
    "accept-web-and-ssh-connections-for-gw-administration": true,
    "accept-web-and-ssh-connections-for-gw-administration-position": "first",
    "accept-incoming-traffic-to-dhcp-and-dns-services-of-gws": true,
    "accept-incoming-traffic-to-dhcp-and-dns-services-of-gws-position": "first",
    "accept-dynamic-addr-modules-outgoing-internet-connections": true,
    "accept-dynamic-addr-modules-outgoing-internet-connections-position": "first",
    "accept-vrrp-packets-originating-from-cluster-members": true,
    "accept-vrrp-packets-originating-from-cluster-members-position": "first",
    "accept-identity-awareness-control-connections": true,
    "accept-identity-awareness-control-connections-position": "first",
    "log-implied-rules": false,
    "security-server": {
      "telnet-welcome-msg-file": "telnetMsgFile",
      "ftp-welcome-msg-file": "ftpMsgFile",
      "rlogin-welcome-msg-file": "RloginMsgFile",
      "client-auth-welcome-file": "clientAuthFile",
      "smtp-welcome-msg": "smtp Msg",
      "mdq-welcome-msg": "mdq Msg",
      "http-next-proxy-host": "nextProxyHost",
      "http-next-proxy-port": 90,
      "http-servers": [
        {
          "logical-name": "logicalName1",
          "host": "hostName1",
          "port": 80,
          "reauthentication": "standard"
        },
        {
          "logical-name": "logicalName2",
          "host": "hostName2",
          "port": 443,
          "reauthentication": "post request"
        }
      ],
      "server-for-null-requests": "logicalName1"
    }
  },
  "nat": {
    "allow-bi-directional-nat": true,
    "auto-translate-dest-on-client-side": true,
    "auto-arp-conf": true,
    "merge-manual-proxy-arp-conf": false,
    "manually-translate-dest-on-client-side": true,
    "enable-ip-pool-nat": false,
    "addr-exhaustion-track": "ip exhaustion log",
    "addr-alloc-and-release-track": "none"
  },
  "authentication": {
    "max-rlogin-attempts-before-connection-termination": 3,
    "max-telnet-attempts-before-connection-termination": 3,
    "max-client-auth-attempts-before-connection-termination": 3,
    "max-session-auth-attempts-before-connection-termination": 3,
    "auth-internal-users-with-specific-suffix": true,
    "allowed-suffix-for-internal-users": "OU=users,O=172.23.26.39-jaguar_155_global1MGMT-ianb.checkpoint.com.86gvfa",
    "max-days-before-expiration-of-non-pulled-user-certificates": 14,
    "enable-delayed-auth": false,
    "delay-each-auth-attempt-by": 100
  },
  "vpn": {
    "vpn-conf-method": "simplified",
    "enable-backup-gw": false,
    "enable-load-distribution-for-mep-conf": false,
    "enable-decrypt-on-accept-for-gw-to-gw-traffic": true,
    "grace-period-before-the-crl-is-valid": 7200,
    "grace-period-after-the-crl-is-not-valid": 1800,
    "grace-period-extension-for-secure-remote-secure-client": 3600,
    "support-ike-dos-protection-from-identified-src": "stateless",
    "support-ike-dos-protection-from-unidentified-src": "puzzles",
    "enable-vpn-directional-match-in-vpn-column": false
  },
  "remote-access": {
    "enable-back-connections": false,
    "keep-alive-packet-to-gw-interval": 0,
    "encrypt-dns-traffic": true,
    "simultaneous-login-mode": "allowonlysinglelogintouser",
    "vpn-authentication-and-encryption": {
      "encryption-method": "ike_v1_only",
      "encryption-algorithms": {
        "ike": {
          "support-encryption-algorithms": {
            "des": true,
            "tdes": true,
            "aes-128": false,
            "aes-256": true
          },
          "use-encryption-algorithm": "aes-256",
          "support-data-integrity": {
            "md5": true,
            "sha1": true,
            "sha256": false,
            "aes-xcbc": false
          },
          "use-data-integrity": "sha1",
          "support-diffie-hellman-groups": {
            "group1": false,
            "group2": true,
            "group5": false,
            "group14": false
          },
          "use-diffie-hellman-group": "group 2"
        },
        "ipsec": {
          "support-encryption-algorithms": {
            "des": false,
            "tdes": false,
            "aes-128": false,
            "aes-256": false
          },
          "use-encryption-algorithm": "3des",
          "support-data-integrity": {
            "md5": false,
            "sha1": false,
            "sha256": false,
            "aes-xcbc": false
          },
          "use-data-integrity": "sha1",
          "enforce-encryption-alg-and-data-integrity-on-all-users": true
        }
      },
      "pre-shared-secret": false,
      "support-legacy-auth-for-sc-l2tp-nokia-clients": true,
      "support-legacy-eap": true,
      "support-l2tp-with-pre-shared-key": false
    },
    "vpn-advanced": {
      "allow-clear-traffic-to-encryption-domain-when-disconnected": true,
      "use-first-allocated-om-ip-addr-for-all-conn-to-the-gws-of-the-site": false,
      "enable-load-distribution-for-mep-conf": false
    },
    "scv": {
      "apply-scv-on-simplified-mode-fw-policies": false,
      "no-scv-for-unsupported-cp-clients": false,
      "upon-verification-accept-and-log-client-connection": false,
      "policy-installed-on-all-interfaces": true,
      "generate-log": true,
      "notify-user": true,
      "only-tcp-ip-protocols-are-used": true
    },
    "ssl-network-extender": {
      "user-auth-method": "legacy",
      "supported-encryption-methods": "3des_only",
      "client-upgrade-upon-connection": "ask_user",
      "client-uninstall-upon-disconnection": "dont_uninstall",
      "scan-ep-machine-for-compliance-with-ep-compliance-policy": false,
      "re-auth-user-interval": 480,
      "client-outgoing-keep-alive-packets-frequency": 20
    },
    "secure-client-mobile": {
      "user-auth-method": "legacy",
      "enable-password-caching": "false",
      "cache-password-timeout": 1440,
      "re-auth-user-interval": 480,
      "connect-mode": "configured on endpoint client",
      "automatically-initiate-dialup": "client_decide",
      "disconnect-when-device-is-idle": "client_decide",
      "supported-encryption-methods": "3des_only",
      "route-all-traffic-to-gw": "false"
    },
    "endpoint-connect": {
      "enable-password-caching": "false",
      "cache-password-timeout": 1440,
      "re-auth-user-interval": 480,
      "connect-mode": "configured on endpoint client",
      "network-location-awareness": "client_decide",
      "disconnect-when-conn-to-network-is-lost": "client_decide",
      "disconnect-when-device-is-idle": "client_decide",
      "route-all-traffic-to-gw": "false",
      "client-upgrade-mode": "ask_user"
    },
    "hot-spot-and-hotel-registration": {
      "enable-registration": false,
      "local-subnets-access-only": false,
      "track-log": false,
      "registration-timeout": 600,
      "max-ip-access-during-registration": 5,
      "ports": [
        "443",
        "80",
        "8080"
      ]
    }
  },
  "user-directory": {
    "enable-password-change-when-user-active-directory-expires": true,
    "timeout-on-cached-users": 900,
    "cache-size": 1000,
    "enable-password-expiration-configuration": false,
    "password-expires-after": 90,
    "display-user-dn-at-login": "no display",
    "min-password-length": 6,
    "password-must-include-lowercase-char": false,
    "password-must-include-uppercase-char": false,
    "password-must-include-a-digit": false,
    "password-must-include-a-symbol": false,
    "enforce-rules-for-user-mgmt-admins": false
  },
  "qos": {
    "max-weight-of-rule": 1000,
    "default-weight-of-rule": 10,
    "unit-of-measure": "kbits-per-sec",
    "authenticated-ip-expiration": 15,
    "non-authenticated-ip-expiration": 5,
    "unanswered-queried-ip-expiration": 3
  },
  "carrier-security": {
    "enforce-gtp-anti-spoofing": true,
    "block-gtp-in-gtp": true,
    "produce-extended-logs-on-unmatched-pdus": false,
    "produce-extended-logs-on-unmatched-pdus-position": "before last",
    "protocol-violation-track-option": "log",
    "verify-flow-labels": true,
    "enable-g-pdu-seq-number-check-with-max-deviation": false,
    "g-pdu-seq-number-check-max-deviation": 16,
    "allow-ggsn-replies-from-multiple-interfaces": true,
    "enable-reverse-connections": true,
    "gtp-signaling-rate-limit-sampling-interval": 1,
    "one-gtp-echo-on-each-path-frequency": 5,
    "aggressive-aging": false,
    "tunnel-activation-threshold": 80,
    "tunnel-deactivation-threshold": 60,
    "memory-activation-threshold": 80,
    "memory-deactivation-threshold": 60,
    "aggressive-timeout": 3600
  },
  "user-accounts": {
    "expiration-date-method": "expire at",
    "expiration-date": {
      "posix": 1924898400000,
      "iso-8601": "2030-12-31T00:00+0200"
    },
    "days-until-expiration": 900,
    "show-accounts-expiration-indication-days-in-advance": true,
    "days-in-advance-to-show-accounts-expiration-indication": 14
  },
  "user-authority": {
    "display-web-access-view": false,
    "windows-domains-to-trust": "all"
  },
  "connect-control": {
    "server-availability-check-interval": 20,
    "server-check-retries": 3,
    "persistence-server-timeout": 1800,
    "load-agents-port": 18212,
    "load-measurement-interval": 20
  },
  "stateful-inspection": {
    "tcp-start-timeout": 25,
    "tcp-session-timeout": 3600,
    "tcp-end-timeout": 20,
    "tcp-end-timeout-r8020-gw-and-above": 5,
    "udp-virtual-session-timeout": 40,
    "icmp-virtual-session-timeout": 30,
    "other-ip-protocols-virtual-session-timeout": 60,
    "sctp-start-timeout": 30,
    "sctp-session-timeout": 3600,
    "sctp-end-timeout": 20,
    "accept-stateful-udp-replies-for-unknown-services": true,
    "accept-stateful-icmp-replies": true,
    "accept-stateful-icmp-errors": true,
    "accept-stateful-other-ip-protocols-replies-for-unknown-services": false,
    "drop-out-of-state-tcp-packets": true,
    "log-on-drop-out-of-state-tcp-packets": true,
    "drop-out-of-state-icmp-packets": true,
    "log-on-drop-out-of-state-icmp-packets": true,
    "drop-out-of-state-sctp-packets": true,
    "log-on-drop-out-of-state-sctp-packets": false
  },
  "log-and-alert": {
    "vpn-successful-key-exchange": "log",
    "vpn-packet-handling-error": "log",
    "vpn-conf-and-key-exchange-errors": "log",
    "ip-options-drop": "none",
    "administrative-notifications": "log",
    "sla-violation": "none",
    "connection-matched-by-sam": "popup alert",
    "packet-is-incorrectly-tagged": "log",
    "packet-tagging-brute-force-attack": "popup alert",
    "log-every-authenticated-http-connection": false,
    "log-traffic": "log",
    "time-settings": {
      "excessive-log-grace-period": 62,
      "logs-resolving-timeout": 20,
      "virtual-link-statistics-logging-interval": 60,
      "status-fetching-interval": 60
    },
    "alerts": {
      "send-popup-alert-to-smartview-monitor": true,
      "send-mail-alert-to-smartview-monitor": false,
      "mail-alert-script": "internal_sendmail -s alert -t mailer root",
      "send-snmp-trap-alert-to-smartview-monitor": false,
      "snmp-trap-alert-script": "internal_snmp_trap localhost",
      "send-user-defined-alert-num1-to-smartview-monitor": true,
      "send-user-defined-alert-num2-to-smartview-monitor": true,
      "send-user-defined-alert-num3-to-smartview-monitor": true,
      "default-track-option-for-system-alerts": "popup alert"
    }
  },
  "data-access-control": {
    "auto-download-important-data": true,
    "auto-download-sw-updates-and-new-features": true,
    "send-anonymous-info": true,
    "share-sensitive-info": false
  },
  "non-unique-ip-address-ranges": [
    {
      "address-type": "ipv4",
      "first-ipv4-address": "10.0.0.0",
      "last-ipv4-address": "10.255.255.255"
    },
    {
      "address-type": "ipv4",
      "first-ipv4-address": "172.16.0.0",
      "last-ipv4-address": "172.31.255.255"
    },
    {
      "address-type": "ipv4",
      "first-ipv4-address": "192.168.0.0",
      "last-ipv4-address": "192.168.255.255"
    }
  ],
  "proxy": {
    "use-proxy-server": false
  },
  "user-check": {
    "preferred-language": "English"
  },
  "hit-count": {
    "enable-hit-count": true,
    "keep-hit-count-data-up-to": "3 months"
  },
  "advanced-conf": {
    "certs-and-pki": {
      "host-certs-key-size": "2048",
      "cert-validation-enforce-key-size": "off",
      "host-certs-ecdsa-key-size": "p-256"
    },
    "keep-ike-sas": true
  },
  "allow-remote-registration-of-opsec-products": false,
  "num-spoofing-errs-that-trigger-brute-force": 3,
  "identity-awareness": {
    "cache-mode": true,
    "cache-mode-duration": 60
  }
}
```
