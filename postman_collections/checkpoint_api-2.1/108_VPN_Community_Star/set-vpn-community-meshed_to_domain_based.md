# set-vpn-community-meshed (to domain based)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-meshed`

## Description

Modifies an existing Star VPN Community to use domain-based routing mode

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "VPN_Community_1",
  "routing-mode": "domain_based"
}
```

## Example Responses

### Example 1: set-vpn-community-meshed (to domain based)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "6bfed9d2-0150-4fac-a712-9811111120f8",
  "name": "VPN_Community_1",
  "type": "vpn-community-star",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "center-gateways": [
    {
      "uid": "035028e5-5f73-45e8-a8cb-1d60d01442fd",
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
      "uid": "937af006-60ef-4546-9d64-b3a798f77101",
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
  "link-selection-mode": "legacy",
  "override-interfaces": [],
  "routing-mode": "domain_based",
  "tunnel-granularity": "per_subnet",
  "use-shared-secret": false,
  "encryption-method": "ikev2 only",
  "encryption-suite": "custom",
  "ike-phase-1": {
    "encryption-algorithm": "aes-256",
    "diffie-hellman-group": "group-15",
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
      "additional-key-exchange-7-methods": [],
      "comments": "Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method",
      "color": "black",
      "icon": "General/globalsNa",
      "tags": [],
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1733867660467,
          "iso-8601": "2024-12-10T23:54+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733867660467,
          "iso-8601": "2024-12-10T23:54+0200"
        },
        "creator": "System"
      },
      "read-only": true,
      "available-actions": {
        "edit": "false",
        "delete": "false",
        "clone": "true"
      }
    },
    "ike-p1-rekey-time": 1440,
    "data-integrity": "sha384"
  },
  "ike-phase-2": {
    "encryption-algorithm": "aes-gcm-128",
    "ike-p2-use-pfs": false,
    "ike-p2-pfs-dh-grp": "group-15",
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
      "additional-key-exchange-7-methods": [],
      "comments": "Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method",
      "color": "black",
      "icon": "General/globalsNa",
      "tags": [],
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1733867660467,
          "iso-8601": "2024-12-10T23:54+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733867660467,
          "iso-8601": "2024-12-10T23:54+0200"
        },
        "creator": "System"
      },
      "read-only": true,
      "available-actions": {
        "edit": "false",
        "delete": "false",
        "clone": "true"
      }
    },
    "ike-p2-rekey-time": 3600,
    "data-integrity": "sha384"
  },
  "comments": "",
  "color": "black",
  "icon": "VPNCommunities/Star",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1733927085402,
      "iso-8601": "2024-12-11T16:24+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1733927055850,
      "iso-8601": "2024-12-11T16:24+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": false,
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "not_supported"
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
