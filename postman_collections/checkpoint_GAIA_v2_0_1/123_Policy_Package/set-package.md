# set-package

**Collection:** Web API (version 2.0.1) > 123 Policy Package
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-package`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Standard",
  "access-layers": {
    "add": [
      {
        "name": "New Access Layer 1",
        "position": 1
      }
    ]
  },
  "threat-layers": {
    "add": [
      {
        "name": "New Layer 1",
        "position": 3
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-package
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7c79f4fe-a02f-4334-9b3f-c9ab65804117",
  "name": "Standard",
  "type": "package",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1682348083974,
      "iso-8601": "2023-04-24T17:54+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1682348083974,
      "iso-8601": "2023-04-24T17:54+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Blades/Access",
  "access": true,
  "access-layers": [
    {
      "uid": "b80a1fec-d67c-4cb8-a4ef-e75a2f6bdc23",
      "name": "New Access Layer 1",
      "type": "access-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    },
    {
      "uid": "9339014e-14a5-46dc-8124-347ff88c78db",
      "name": "Network",
      "type": "access-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    }
  ],
  "threat-layers": [
    {
      "uid": "d31d7386-755f-45c7-9727-88153d3375c2",
      "name": "IPS",
      "type": "threat-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/sharedrulebase",
      "color": "black"
    },
    {
      "uid": "c632e26f-6b35-4d5c-bcc3-2bb0a7e6e438",
      "name": "Standard Threat Prevention",
      "type": "threat-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    },
    {
      "uid": "d0b6d03a-7757-4569-a206-25cde3842dc3",
      "name": "New Layer 1",
      "type": "threat-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    },
    {
      "uid": "86ff3b87-5cfa-468f-a519-5a86508f57d8",
      "name": "L1",
      "type": "threat-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/sharedrulebase",
      "color": "black"
    }
  ],
  "vpn-traditional-mode": false,
  "nat-policy": true,
  "qos": false,
  "qos-policy-type": "recommended",
  "desktop-security": false,
  "threat-prevention": true,
  "installation-targets": "all",
  "https-inspection-policy": true,
  "autonomous-threat-policy": "e6bc98ae-7e20-43ff-8e65-b9b80a3a50de",
  "https-inspection-layers": {
    "inbound-https-layer": {
      "uid": "7ec7bcea-3d84-4dde-9b4b-6a057845d26c",
      "name": "Default Inbound Layer",
      "type": "https-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    },
    "outbound-https-layer": {
      "uid": "97b6c38c-18a8-40d5-93fb-a114028f2dd6",
      "name": "Default Outbound Layer",
      "type": "https-layer",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "ApplicationFirewall/rulebase",
      "color": "black"
    }
  },
  "infinity-threat-policy": "e6bc98ae-7e20-43ff-8e65-b9b80a3a50de"
}
```
