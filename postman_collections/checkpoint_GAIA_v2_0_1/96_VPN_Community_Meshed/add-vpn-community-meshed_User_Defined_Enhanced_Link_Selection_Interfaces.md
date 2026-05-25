# add-vpn-community-meshed (User Defined Enhanced Link Selection Interfaces)

**Collection:** Web API (version 2.0.1) > 96 VPN Community Meshed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-vpn-community-meshed`

## Description

Adds a new VPN Meshed Community with user defined Enhanced Link Selection Interfaces configuration

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_VPN_Community_Meshed_With_User_Defined_Enhanced_Link_Selection_Interfaces",
  "gateways": [
    "Gateway_1_version_R82_Meshed",
    "Gateway_2_version_R82_Meshed"
  ],
  "override-interfaces": [
    {
      "gateway": "Gateway_1_version_R82_Meshed",
      "interfaces": [
        {
          "interface-name": "eth2",
          "next-hop-ip": "172.43.52.100",
          "static-nat-ip": "10.20.30.10",
          "redundancy-mode": "active"
        },
        {
          "interface-name": "eth0",
          "next-hop-ip": "172.23.42.100",
          "static-nat-ip": "50.40.30.10",
          "redundancy-mode": "backup",
          "priority": "7"
        }
      ]
    },
    {
      "gateway": "Gateway_2_version_R82_Meshed",
      "interfaces": [
        {
          "interface-name": "eth2",
          "next-hop-ip": "172.43.52.100",
          "static-nat-ip": "5.9.8.6",
          "redundancy-mode": "active"
        },
        {
          "interface-name": "eth0",
          "next-hop-ip": "172.23.42.100",
          "static-nat-ip": "1.2.5.6",
          "redundancy-mode": "backup",
          "priority": "2"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: add-vpn-community-meshed (User Defined Enhanced Link Selection Interfaces)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "55dbba16-9e0f-4572-8917-46522b8df256",
  "name": "New_VPN_Community_Meshed_With_User_Defined_Enhanced_Link_Selection_Interfaces",
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
      "posix": 1717508931200,
      "iso-8601": "2024-06-04T16:48+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1717508931200,
      "iso-8601": "2024-06-04T16:48+0300"
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
        "uid": "881221f2-57c8-4fc2-9278-213c582722a6",
        "name": "Gateway_1_version_R82_Meshed",
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
        "uid": "b6778957-bc72-4e63-b46f-8ba26952fb05",
        "name": "Gateway_2_version_R82_Meshed",
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
    }
  ],
  "gateways": [
    {
      "uid": "b6778957-bc72-4e63-b46f-8ba26952fb05",
      "name": "Gateway_2_version_R82_Meshed",
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
      "uid": "881221f2-57c8-4fc2-9278-213c582722a6",
      "name": "Gateway_1_version_R82_Meshed",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black"
    }
  ]
}
```
