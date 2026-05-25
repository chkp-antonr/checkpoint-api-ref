# set-vpn-community-star (add Enhanced Link Selection Interfaces)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-vpn-community-star`

## Description

Modifies an existing VPN Star Community with Enhanced Link Selection Interfaces (Add Action)

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_VPN_Community_Star_With_User_Defined_Enhanced_Link_Selection_Interfaces",
  "center-gateways": {
    "add": [
      "Gateway_3_version_R82_Starred"
    ]
  },
  "override-interfaces": {
    "add": [
      {
        "gateway": "Gateway_3_version_R82_Starred",
        "interfaces": {
          "interface-name": "eth2"
        }
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-vpn-community-star (add Enhanced Link Selection Interfaces)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "051cd8c9-6ef8-4796-ace9-ab0a89f5889b",
  "name": "New_VPN_Community_Star_With_User_Defined_Enhanced_Link_Selection_Interfaces",
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
      "posix": 1717665021828,
      "iso-8601": "2024-06-06T12:10+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1717664821229,
      "iso-8601": "2024-06-06T12:07+0300"
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
  "link-selection-mode": "enhanced",
  "override-interfaces": [
    {
      "gateway": {
        "uid": "02840bd3-1abb-4a04-b187-c1e7ee44eb69",
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
      "interfaces": [
        {
          "interface-name": "eth2",
          "next-hop-ip": "172.43.52.100",
          "static-nat-ip": "10.20.30.10",
          "redundancy-mode": "active",
          "ip-version": "ipv4"
        },
        {
          "interface-name": "eth0",
          "next-hop-ip": "172.23.42.100",
          "static-nat-ip": "50.40.30.10",
          "priority": 7,
          "redundancy-mode": "backup",
          "ip-version": "ipv4"
        }
      ]
    },
    {
      "gateway": {
        "uid": "bb95cc43-ae95-4f72-8ba5-2aa861f18368",
        "name": "Gateway_2_version_R82_Starred",
        "type": "simple-gateway",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      },
      "interfaces": [
        {
          "interface-name": "eth2",
          "next-hop-ip": "172.43.52.100",
          "static-nat-ip": "5.9.8.6",
          "redundancy-mode": "active",
          "ip-version": "ipv4"
        },
        {
          "interface-name": "eth0",
          "next-hop-ip": "172.23.42.100",
          "static-nat-ip": "1.2.5.6",
          "priority": 2,
          "redundancy-mode": "backup",
          "ip-version": "ipv4"
        }
      ]
    },
    {
      "gateway": {
        "uid": "793d350f-0a4b-4c7a-b07c-893bd8091b02",
        "name": "Gateway_3_version_R82_Starred",
        "type": "simple-gateway",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      },
      "interfaces": [
        {
          "interface-name": "eth2",
          "redundancy-mode": "active",
          "ip-version": "ipv4"
        }
      ]
    }
  ],
  "routing-mode": "domain_based",
  "center-gateways": [
    {
      "uid": "02840bd3-1abb-4a04-b187-c1e7ee44eb69",
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
      "uid": "793d350f-0a4b-4c7a-b07c-893bd8091b02",
      "name": "Gateway_3_version_R82_Starred",
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
      "uid": "bb95cc43-ae95-4f72-8ba5-2aa861f18368",
      "name": "Gateway_2_version_R82_Starred",
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
