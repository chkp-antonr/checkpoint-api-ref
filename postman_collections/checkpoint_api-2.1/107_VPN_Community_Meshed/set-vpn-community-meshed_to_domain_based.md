# set-vpn-community-meshed (to domain based)

**Collection:** Web API (version 2.1) > 107 VPN Community Meshed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-meshed`

## Description

Modifies an existing Meshed VPN Community to use domain-based routing mode

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
  "uid": "48aaacde-b76a-4063-b832-fcd02c6fecbd",
  "name": "VPN_Community_1",
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
      "posix": 1733837518666,
      "iso-8601": "2024-12-10T15:31+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1733836678120,
      "iso-8601": "2024-12-10T15:17+0200"
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
          "posix": 1733226684395,
          "iso-8601": "2024-12-03T13:51+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733226684395,
          "iso-8601": "2024-12-03T13:51+0200"
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
          "posix": 1733226684395,
          "iso-8601": "2024-12-03T13:51+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1733226684395,
          "iso-8601": "2024-12-03T13:51+0200"
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
  "routing-mode": "domain_based",
  "gateways": [
    {
      "uid": "a13e945c-13db-456a-a35b-c2e78423240a",
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
      "uid": "9915327c-33db-4a0d-8c2f-abec0acb0140",
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
    "override-routes": [],
    "advanced": {
      "bfd": false,
      "graceful-restart": true
    }
  }
}
```
