# add-vpn-community-star (override dynamic routing settings)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-vpn-community-star`

## Description

Adds a new Route Based Star VPN Community with override dynamic routing settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "RouteBased_Star_VPN_Community",
  "routing-mode": "route_based",
  "center-gateways": [
    "gateway_1"
  ],
  "satellite-gateways": [
    "gateway_2"
  ],
  "route-based-settings": {
    "override-routes": [
      {
        "gateway": "gateway_1",
        "auto-config": false
      }
    ]
  }
}
```

## Example Responses

### Example 1: add-vpn-community-star (override dynamic routing settings)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a49fe74f-79ab-4f13-8f5f-61028bd3bbed",
  "name": "RouteBased_Star_VPN_Community",
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
      "posix": 1753969391246,
      "iso-8601": "2025-07-31T16:43+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1753969391246,
      "iso-8601": "2025-07-31T16:43+0300"
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
    "enabled": false,
    "community-members": "both center and satellite gateways"
  },
  "permanent-tunnels": {
    "set-permanent-tunnels": "off",
    "tunnel-down-track": "log",
    "tunnel-up-track": "log",
    "gateways": [],
    "tunnels": [],
    "rim": {
      "enabled": false,
      "enable-on-center-gateways": true,
      "enable-on-satellite-gateways": false,
      "center-gw-costumer-editable-script-exec": false,
      "satellite-gw-costumer-editable-script-exec": false,
      "route-injection-track": "log"
    }
  },
  "center-gateways": [
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
  "satellite-gateways": [
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
    }
  ],
  "mesh-center-gateways": false,
  "disable-nat-on": "both center and satellite gateways",
  "vpn-routing": "to center only",
  "mep": {
    "enabled": false,
    "entry-point-selection-mechanism": "closest gateway to source",
    "entry-point-final-selection-mechanism": "first to respond",
    "tracking": "log",
    "default-priority-rule": {
      "satellite-gateways": [
        {
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
          "name": "Any",
          "type": "CpmiAnyObject",
          "domain": {
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data",
            "domain-type": "data domain"
          },
          "icon": "General/globalsAny",
          "color": "black"
        }
      ],
      "first-priority-center-gateways": [],
      "second-priority-center-gateways": [],
      "third-priority-center-gateways": []
    }
  },
  "route-based-settings": {
    "add-automatic-routes": "bgp",
    "advanced": {
      "bfd": false,
      "graceful-restart": true
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
        "auto-config": false,
        "mode": "according_to_gateway",
        "exported-routes": {
          "internal-interfaces": true,
          "static-routes": false,
          "custom-routes": false
        }
      }
    ]
  }
}
```
