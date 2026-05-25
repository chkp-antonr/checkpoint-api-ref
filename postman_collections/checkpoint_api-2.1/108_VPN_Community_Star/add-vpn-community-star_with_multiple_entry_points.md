# add-vpn-community-star (with multiple entry points)

**Collection:** Web API (version 2.1) > 108 VPN Community Star
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-vpn-community-star`

## Description

Adds a new VPN Star Community with Multiple Entry Points.

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
  "center-gateways": [
    "centerGW1",
    "centerGW2",
    "centerGW3",
    "centerGW4"
  ],
  "satellite-gateways": [
    "satGW1",
    "satGW2",
    "satGW3"
  ],
  "link-selection-mode": "legacy",
  "mep": {
    "enabled": true,
    "entry-point-selection-mechanism": "manual",
    "default-priority-rule": {
      "first-priority-center-gateways": [
        "centerGW1",
        "centerGW2"
      ],
      "second-priority-center-gateways": "centerGW3",
      "third-priority-center-gateways": "centerGW4"
    },
    "exception-priority-rules": [
      {
        "satellite-gateways": [
          "satGW1",
          "satGW2"
        ],
        "first-priority-center-gateways": [
          "centerGW1",
          "centerGW2"
        ],
        "second-priority-center-gateways": "centerGW3",
        "third-priority-center-gateways": "None"
      }
    ],
    "tracking": "user defined alert no.2"
  }
}
```

## Example Responses

### Example 1: add-vpn-community-star (with multiple entry points)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5d5ee284-dbe7-4bbc-ada4-2893d5680bc7",
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
      "posix": 1736887782416,
      "iso-8601": "2025-01-14T22:49+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1736887782416,
      "iso-8601": "2025-01-14T22:49+0200"
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
  "routing-mode": "domain_based",
  "center-gateways": [
    {
      "uid": "cfb98d59-713d-463b-8cbb-af463de8e293",
      "name": "centerGW4",
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
    },
    {
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
    "enabled": true,
    "entry-point-selection-mechanism": "manual",
    "entry-point-final-selection-mechanism": "first to respond",
    "tracking": "user defined alert no.2",
    "exception-priority-rules": [
      {
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
        "first-priority-center-gateways": [
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
        "second-priority-center-gateways": [
          {
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
          }
        ],
        "third-priority-center-gateways": [
          {
            "uid": "97aeb36a-9aea-11d5-bd16-0090272ccb30",
            "name": "None",
            "type": "CpmiAnyObject",
            "domain": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "domain-type": "data domain"
            },
            "icon": "General/globalsNone",
            "color": "black"
          }
        ]
      }
    ],
    "default-priority-rule": {
      "first-priority-center-gateways": [
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
      "second-priority-center-gateways": [
        {
          "uid": "97aeb36a-9aea-11d5-bd16-0090272ccb30",
          "name": "None",
          "type": "CpmiAnyObject",
          "domain": {
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data",
            "domain-type": "data domain"
          },
          "icon": "General/globalsNone",
          "color": "black"
        }
      ],
      "third-priority-center-gateways": [
        {
          "uid": "97aeb36a-9aea-11d5-bd16-0090272ccb30",
          "name": "None",
          "type": "CpmiAnyObject",
          "domain": {
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data",
            "domain-type": "data domain"
          },
          "icon": "General/globalsNone",
          "color": "black"
        }
      ]
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
