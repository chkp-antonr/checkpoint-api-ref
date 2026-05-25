# set-vpn-community-star (remove permanent tunnel)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-star`

## Description

Modifies an existing VPN Star Community with permanent tunnel (Remove Action)

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vpnCommunityStar",
  "permanent-tunnels": {
    "tunnels": {
      "remove": {
        "first-tunnel-endpoint": "centerGW2",
        "second-tunnel-endpoint": "satGW2"
      }
    }
  }
}
```

## Example Responses

### Example 1: set-vpn-community-star (remove permanent tunnel)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f3ffa6d0-4e6e-4254-b260-e64a4f53912a",
  "name": "vpnCommunityStar",
  "type": "vpn-community-star",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1736886638788,
      "iso-8601": "2025-01-14T22:30+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1736886175079,
      "iso-8601": "2025-01-14T22:22+0200"
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
  "icon": "VPNCommunities/Star",
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
    "set-permanent-tunnels": "on specific tunnels in the community",
    "tunnel-down-track": "log",
    "tunnel-up-track": "log",
    "gateways": [],
    "tunnels": [
      {
        "first-tunnel-endpoint": {
          "uid": "184c53e4-6fed-450a-9e79-baac108703b2",
          "name": "centerGW1",
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
        "second-tunnel-endpoint": {
          "uid": "e0d0c327-43a9-4e1e-971b-6ee83b78105a",
          "name": "satGW1",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        },
        "track-options": "override track options"
      },
      {
        "first-tunnel-endpoint": {
          "uid": "72ad02ec-b735-435b-b02b-1c45bacdaa85",
          "name": "centerGW3",
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
        "second-tunnel-endpoint": {
          "uid": "62a2e2cf-8372-4ac7-bd27-f268eae725ca",
          "name": "satGW3",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        },
        "track-options": "according to community track options"
      }
    ],
    "rim": {
      "enabled": false,
      "enable-on-center-gateways": false,
      "enable-on-satellite-gateways": false,
      "center-gw-costumer-editable-script-exec": false,
      "satellite-gw-costumer-editable-script-exec": false,
      "route-injection-track": "none"
    }
  },
  "routing-mode": "domain_based",
  "center-gateways": [
    {
      "uid": "cce61c09-6319-4219-a487-134fd0a4e45b",
      "name": "centerGW2",
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
      "uid": "184c53e4-6fed-450a-9e79-baac108703b2",
      "name": "centerGW1",
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
  "satellite-gateways": [
    {
      "uid": "e0d0c327-43a9-4e1e-971b-6ee83b78105a",
      "name": "satGW1",
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
      "uid": "7e572d86-19e8-49ca-88d3-baad72a04c0f",
      "name": "satGW2",
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
  "mesh-center-gateways": false,
  "disable-nat-on": "both center and satellite gateways",
  "encrypted-traffic": {
    "enabled": false,
    "community-members": "both center and satellite gateways"
  },
  "vpn-routing": "to center only",
  "mep": {
    "enabled": false,
    "entry-point-selection-mechanism": "closest gateway to source",
    "entry-point-final-selection-mechanism": "first to respond",
    "tracking": "log",
    "default-priority-rule": {
      "first-priority-center-gateways": [],
      "second-priority-center-gateways": [],
      "third-priority-center-gateways": []
    }
  },
  "route-based-settings": {
    "add-automatic-routes": "bgp",
    "override-routes": [],
    "advanced": {
      "bfd": false,
      "graceful-restart": true
    }
  }
}
```
