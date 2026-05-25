# set-vpn-community-star (replace granular encryption)

**Collection:** Web API (version 2.0.1) > 97 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-vpn-community-star`

## Description

Modifies an existing VPN Star Community with Granular Encryption (Replace Action)

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_VPN_Community_Star_With_Granular_Encryption",
  "granular-encryptions": [
    {
      "internal-gateway": "Gateway_1_version_R82_Starred",
      "external-gateway": "External_Gateway_1",
      "encryption-suite": "custom",
      "encryption-method": "prefer ikev2 but support ikev1",
      "ike-phase-1": {
        "data-integrity": "sha256",
        "encryption-algorithm": "aes-256",
        "diffie-hellman-group": "group-19",
        "ike-p1-rekey-time": 1200
      },
      "ike-phase-2": {
        "data-integrity": "sha384",
        "encryption-algorithm": "aes-gcm-128",
        "ike-p2-pfs-dh-grp": "group-19",
        "ike-p2-rekey-time": 3000,
        "ike-p2-use-pfs": true
      }
    }
  ]
}
```

## Example Responses

### Example 1: set-vpn-community-star (replace granular encryption)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1489512e-7687-48f9-a492-ccf367ab90ef",
  "name": "New_VPN_Community_Star_With_Granular_Encryption",
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
      "posix": 1717597485205,
      "iso-8601": "2024-06-05T17:24+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1717586885158,
      "iso-8601": "2024-06-05T14:28+0300"
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
  "granular-encryptions": [
    {
      "internal-gateway": {
        "uid": "4a1b7034-0b01-4a8c-b793-6d85ae501f65",
        "name": "Gateway_1_version_R82_Starred",
        "type": "simple-gateway",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      },
      "external-gateway": {
        "uid": "2893aa8e-440c-4af6-8b57-d58e40d51728",
        "name": "External_Gateway_1",
        "type": "interoperable-device",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      },
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
        "encryption-algorithm": "aes-256",
        "diffie-hellman-group": "group-19",
        "ike-p1-rekey-time": 1200,
        "data-integrity": "sha256"
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
        "ike-p2-pfs-dh-grp": "group-19",
        "ike-p2-use-pfs": true,
        "ike-p2-rekey-time": 3000,
        "data-integrity": "sha384"
      }
    }
  ],
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
    "data-integrity": "sha384"
  },
  "link-selection-mode": "legacy",
  "override-interfaces": [],
  "center-gateways": [
    {
      "uid": "4a1b7034-0b01-4a8c-b793-6d85ae501f65",
      "name": "Gateway_1_version_R82_Starred",
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
      "uid": "2893aa8e-440c-4af6-8b57-d58e40d51728",
      "name": "External_Gateway_1",
      "type": "interoperable-device",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    }
  ],
  "satellite-gateways": [],
  "mesh-center-gateways": false
}
```
