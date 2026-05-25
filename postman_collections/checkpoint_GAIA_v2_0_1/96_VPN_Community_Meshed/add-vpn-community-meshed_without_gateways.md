# add-vpn-community-meshed (without gateways)

**Collection:** Web API (version 2.0.1) > 96 VPN Community Meshed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-vpn-community-meshed`

## Description

Adds a new VPN Meshed Community

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_VPN_Community_Meshed_Without_Gateways",
  "encryption-method": "prefer ikev2 but support ikev1",
  "encryption-suite": "custom",
  "ike-phase-1": {
    "data-integrity": "sha1",
    "encryption-algorithm": "aes-128",
    "diffie-hellman-group": "group 19"
  },
  "ike-phase-2": {
    "data-integrity": "aes-xcbc",
    "encryption-algorithm": "aes-gcm-128"
  }
}
```

## Example Responses

### Example 1: add-vpn-community-meshed (without gateways)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3f3d178f-dc5f-43bd-afcd-e88b993e010c",
  "name": "New_VPN_Community_Meshed_Without_Gateways",
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
      "posix": 1717507866049,
      "iso-8601": "2024-06-04T16:31+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1717507866049,
      "iso-8601": "2024-06-04T16:31+0300"
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
  "encryption-method": "prefer ikev2 but support ikev1",
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
          "posix": 1715194335001,
          "iso-8601": "2024-05-08T21:52+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1715194335001,
          "iso-8601": "2024-05-08T21:52+0300"
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
    "encryption-algorithm": "aes-128",
    "diffie-hellman-group": "group-19",
    "ike-p1-rekey-time": 1440,
    "data-integrity": "sha1"
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
          "posix": 1715194335001,
          "iso-8601": "2024-05-08T21:52+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1715194335001,
          "iso-8601": "2024-05-08T21:52+0300"
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
    "data-integrity": "aes-xcbc"
  },
  "link-selection-mode": "enhanced",
  "override-interfaces": [],
  "gateways": []
}
```
