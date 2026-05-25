# show-gateway-capabilities for platform smb

**Collection:** Web API (version 2.0.1) > 54 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-gateway-capabilities`

## Description

Show supported gateway capabilities for a specified platform

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "platform": "smb"
}
```

## Example Responses

### Example 1: show-gateway-capabilities for platform smb
**Status:** `200 OK`

**Body:**
```javascript
{
  "restrictions": {
    "platform": "smb",
    "version": "any",
    "hardware": "any"
  },
  "supported-platforms": {
    "platforms": [
      "smb"
    ],
    "default": "smb"
  },
  "supported-versions": {
    "versions": [
      "R75.20",
      "R77.20",
      "R80.20",
      "R81.10"
    ],
    "default": "R81.10"
  },
  "supported-blades": {
    "network-security": [
      {
        "name": "Dynamic Routing",
        "readonly": true,
        "default": true
      },
      {
        "name": "QoS",
        "readonly": false,
        "default": false
      },
      {
        "name": "Application Control",
        "readonly": false,
        "default": false
      },
      {
        "name": "SecureXL",
        "readonly": true,
        "default": true
      },
      {
        "name": "Anti-Spam & Email Security",
        "readonly": false,
        "default": false
      },
      {
        "name": "IPSec VPN",
        "readonly": false,
        "default": false
      },
      {
        "name": "URL Filtering",
        "readonly": false,
        "default": false
      },
      {
        "name": "Identity Awareness",
        "readonly": false,
        "default": false
      },
      {
        "name": "Firewall",
        "readonly": false,
        "default": true
      }
    ],
    "threat-prevention": {
      "custom": [
        {
          "name": "Threat Extraction",
          "readonly": false,
          "default": false
        },
        {
          "name": "Anti-Bot",
          "readonly": false,
          "default": false
        },
        {
          "name": "Threat Emulation",
          "readonly": false,
          "default": false
        },
        {
          "name": "Zero Phishing",
          "readonly": false,
          "default": false
        },
        {
          "name": "Anti-Virus",
          "readonly": false,
          "default": false
        },
        {
          "name": "IPS",
          "readonly": false,
          "default": false
        }
      ],
      "autonomous": []
    }
  },
  "supported-hardware": {
    "hardware": [
      "1100 Appliances",
      "1200R Appliances",
      "1430/1450 Appliances",
      "1470/1490 Appliances",
      "1530/1550 Appliances",
      "1570/1590 Appliances",
      "1570R Appliances",
      "1600 Appliances",
      "1800 Appliances",
      "Quantum Edge"
    ],
    "default": "1100 Appliances"
  }
}
```
