# set-vpn-community-star (use multiple key exchange)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-vpn-community-star`

## Description

Modifies an existing VPN Star Community with Multiple Key Exchange

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_VPN_Community_Star_With_Multiple_Key_Exchange",
  "link-selection-mode": "legacy",
  "ike-phase-1": {
    "use-multiple-key-exchanges": "true",
    "multiple-key-exchanges": "Default Multiple Key Exchanges"
  }
}
```

## Example Responses

### Example 1: set-vpn-community-star (use multiple key exchange)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1f545cee-026b-4a11-8502-d37d84b0d319",
  "name": "New_VPN_Community_Star_With_Multiple_Key_Exchange",
  "type": "vpn-community-star",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "routing-mode": "domain_based",
  "center-gateways": [],
  "satellite-gateways": [],
  "mesh-center-gateways": false,
  "link-selection-mode": "legacy",
  "override-interfaces": [],
  "tunnel-granularity": "per_subnet",
  "use-shared-secret": false,
  "encryption-method": "ikev2 only",
  "encryption-suite": "custom",
  "ike-phase-1": {
    "encryption-algorithm": "aes-256",
    "diffie-hellman-group": "group-15",
    "use-standard-proposal": true,
    "use-multiple-key-exchanges": true,
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
          "posix": 1733921780209,
          "iso-8601": "2024-12-11T14:56+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733921780209,
          "iso-8601": "2024-12-11T14:56+0200"
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
          "posix": 1733921780209,
          "iso-8601": "2024-12-11T14:56+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733921780209,
          "iso-8601": "2024-12-11T14:56+0200"
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
      "posix": 1734024623422,
      "iso-8601": "2024-12-12T19:30+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1734024620179,
      "iso-8601": "2024-12-12T19:30+0200"
    },
    "creator": "WEB_API"
  },
  "read-only": true,
  "available-actions": {
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
