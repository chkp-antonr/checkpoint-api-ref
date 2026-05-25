# set-vpn-community-meshed (override dynamic routing settings)

**Collection:** Web API (version 2.1) > 107 VPN Community Meshed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-meshed`

## Description

Modifies an existing VPN Meshed Community with override dynamic routing settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "RouteBased_Meshed_VPN_Community",
  "route-based-settings": {
    "override-routes": [
      {
        "gateway": "gateway_1",
        "mode": "override",
        "exported-routes": {
          "custom-routes": true,
          "custom-routes-object": "my_network"
        }
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-vpn-community-meshed (override dynamic routing settings)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1c54647d-f078-4498-a489-4c58224f2361",
  "name": "RouteBased_Meshed_VPN_Community",
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
      "posix": 1753969685607,
      "iso-8601": "2025-07-31T16:48+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1753968885208,
      "iso-8601": "2025-07-31T16:34+0300"
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
  "icon": "VPNCommunities/Meshed",
  "use-shared-secret": false,
  "tunnel-granularity": "universal",
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
          "posix": 1753107579401,
          "iso-8601": "2025-07-21T17:19+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1753107579401,
          "iso-8601": "2025-07-21T17:19+0300"
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
          "posix": 1753107579401,
          "iso-8601": "2025-07-21T17:19+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1753107579401,
          "iso-8601": "2025-07-21T17:19+0300"
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
  "link-selection-mode": "enhanced",
  "override-interfaces": [],
  "routing-mode": "route_based",
  "disable-nat": false,
  "excluded-services": [],
  "wire-mode": {
    "allow-uninspected-encrypted-traffic": false,
    "allow-uninspected-encrypted-routing": false
  },
  "advanced-properties": {
    "use-aggressive-mode": false,
    "support-ip-compression": false
  },
  "encrypted-traffic": {
    "enabled": false
  },
  "permanent-tunnels": {
    "set-permanent-tunnels": "off",
    "tunnel-down-track": "log",
    "tunnel-up-track": "log",
    "gateways": [],
    "tunnels": [],
    "rim": {
      "enabled": false,
      "enable-on-gateways": true,
      "gw-costumer-editable-script-exec": false,
      "route-injection-track": "log"
    }
  },
  "gateways": [
    {
      "uid": "02d5a556-5473-4925-acde-b964a1d686cc",
      "name": "gateway_2",
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
      "uid": "8d0e17d8-d73f-48d5-9794-2b55c9444437",
      "name": "gateway_1",
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
  "route-based-settings": {
    "add-automatic-routes": "bgp",
    "advanced": {
      "bfd": true,
      "graceful-restart": false
    },
    "override-routes": [
      {
        "gateway": {
          "uid": "8d0e17d8-d73f-48d5-9794-2b55c9444437",
          "name": "gateway_1",
          "type": "simple-gateway",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "icon": "NetworkObjects/gateway",
          "color": "black"
        },
        "auto-config": true,
        "mode": "override",
        "exported-routes": {
          "internal-interfaces": true,
          "static-routes": false,
          "custom-routes": true,
          "custom-routes-object": {
            "uid": "8f119dbf-e6dc-49d8-9a11-cc570aa731e6",
            "name": "my_network",
            "type": "network",
            "domain": {
              "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
              "name": "SMC User",
              "domain-type": "domain"
            },
            "icon": "NetworkObjects/network",
            "color": "black",
            "subnet4": "30.30.30.0",
            "subnet-mask": "255.255.255.0",
            "mask-length4": 24
          }
        }
      }
    ]
  }
}
```
