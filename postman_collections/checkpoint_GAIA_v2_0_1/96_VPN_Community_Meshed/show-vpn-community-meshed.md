# show-vpn-community-meshed

**Collection:** Web API (version 2.0.1) > 96 VPN Community Meshed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-vpn-community-meshed`

## Description

Displays a VPN Meshed Community

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vpnCommunityMeshed"
}
```

## Example Responses

### Example 1: show-vpn-community-meshed
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4141323b-c34c-487b-8d31-27ed6db010b5",
  "name": "vpnCommunityMeshed",
  "type": "vpn-community-meshed",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1736931400387,
      "iso-8601": "2025-01-15T10:56+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1736931400387,
      "iso-8601": "2025-01-15T10:56+0200"
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
  "color": "black",
  "icon": "VPNCommunities/Meshed",
  "use-shared-secret": false,
  "tunnel-granularity": "per_subnet",
  "encryption-method": "ikev2 only",
  "encryption-suite": "custom",
  "ike-phase-1": {
    "use-standard-proposal": true,
    "use-multiple-key-exchanges": false,
    "multiple-key-exchanges": {
      "uid": "3edc642d-f613-4d39-b1a8-d38603cf7fd5",
      "name": "Default Multiple Key Exchanges",
      "type": "multiple-key-exchanges",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1734364762484,
          "iso-8601": "2024-12-16T17:59+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1734364762484,
          "iso-8601": "2024-12-16T17:59+0200"
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
      "comments": "Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method",
      "color": "black",
      "icon": "General/globalsNa",
      "key-exchange-methods": [
        "group-15"
      ],
      "additional-key-exchange-1-methods": [
        "kyber-768"
      ],
      "additional-key-exchange-2-methods": [],
      "additional-key-exchange-3-methods": [],
      "additional-key-exchange-4-methods": [],
      "additional-key-exchange-5-methods": [],
      "additional-key-exchange-6-methods": [],
      "additional-key-exchange-7-methods": []
    },
    "encryption-algorithm": "aes-256",
    "diffie-hellman-group": "group-15",
    "ike-p1-rekey-time": 1440,
    "data-integrity": "sha384"
  },
  "ike-phase-2": {
    "use-standard-proposal": true,
    "use-multiple-key-exchanges": false,
    "multiple-key-exchanges": {
      "uid": "3edc642d-f613-4d39-b1a8-d38603cf7fd5",
      "name": "Default Multiple Key Exchanges",
      "type": "multiple-key-exchanges",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1734364762484,
          "iso-8601": "2024-12-16T17:59+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1734364762484,
          "iso-8601": "2024-12-16T17:59+0200"
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
      "comments": "Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method",
      "color": "black",
      "icon": "General/globalsNa",
      "key-exchange-methods": [
        "group-15"
      ],
      "additional-key-exchange-1-methods": [
        "kyber-768"
      ],
      "additional-key-exchange-2-methods": [],
      "additional-key-exchange-3-methods": [],
      "additional-key-exchange-4-methods": [],
      "additional-key-exchange-5-methods": [],
      "additional-key-exchange-6-methods": [],
      "additional-key-exchange-7-methods": []
    },
    "encryption-algorithm": "aes-gcm-128",
    "ike-p2-pfs-dh-grp": "group-15",
    "ike-p2-use-pfs": false,
    "ike-p2-rekey-time": 3600,
    "data-integrity": "sha384"
  },
  "link-selection-mode": "legacy",
  "override-interfaces": [],
  "disable-nat": false,
  "excluded-services": [],
  "wire-mode": {
    "allow-uninspected-encrypted-traffic": false,
    "allow-uninspected-encrypted-routing": false
  },
  "permanent-tunnels": {
    "set-permanent-tunnels": "on all tunnels of specific gateways",
    "tunnel-down-track": "log",
    "tunnel-up-track": "log",
    "gateways": [
      {
        "gateway": {
          "uid": "91be63f1-b5f2-4490-8990-936a9b4d4da7",
          "name": "gw1",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        },
        "override-tunnel-down-track": "mail alert",
        "override-tunnel-up-track": "log",
        "track-options": "override track options"
      },
      {
        "gateway": {
          "uid": "4cc74e11-7f53-40b2-8df6-0a2da662cdf6",
          "name": "gw2",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        },
        "override-tunnel-down-track": "log",
        "override-tunnel-up-track": "log",
        "track-options": "according to community track options"
      }
    ],
    "tunnels": [],
    "rim": {
      "enabled": true,
      "enable-on-gateways": true,
      "gw-costumer-editable-script-exec": false,
      "route-injection-track": "popup alert"
    }
  },
  "routing-mode": "domain_based",
  "gateways": [
    {
      "uid": "9cc56b69-ff84-4efd-be5a-fcfc8a51e555",
      "name": "gw4",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    },
    {
      "uid": "4cc74e11-7f53-40b2-8df6-0a2da662cdf6",
      "name": "gw2",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    },
    {
      "uid": "91be63f1-b5f2-4490-8990-936a9b4d4da7",
      "name": "gw1",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    },
    {
      "uid": "2c6b9cf3-415a-49ca-831a-700afa19352e",
      "name": "gw3",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    }
  ],
  "encrypted-traffic": {
    "enabled": false
  }
}
```
