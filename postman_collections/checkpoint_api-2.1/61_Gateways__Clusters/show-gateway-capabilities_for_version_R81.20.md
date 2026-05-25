# show-gateway-capabilities for version R81.20

**Collection:** Web API (version 2.1) > 61 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-gateway-capabilities`

## Description

Show supported gateway capabilities for a specified version

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "version": "R81.20"
}
```

## Example Responses

### Example 1: show-gateway-capabilities for version R81.20
**Status:** `200 OK`

**Body:**
```javascript
{
  "restrictions": {
    "version": "R81.20",
    "hardware": "any"
  },
  "supported-platforms": {
    "platforms": [
      "quantum",
      "open server",
      "maestro"
    ],
    "default": "open server"
  },
  "supported-versions": {
    "versions": [
      "R81.20"
    ],
    "default": "R81.20"
  },
  "supported-blades": {
    "management": [
      {
        "name": "Identity Logging",
        "readonly": true,
        "default": false
      },
      {
        "name": "Network Policy Management",
        "readonly": false,
        "default": false
      },
      {
        "name": "Endpoint Policy Management",
        "readonly": false,
        "default": false
      },
      {
        "name": "Compliance",
        "readonly": true,
        "default": false
      },
      {
        "name": "Secondary Server",
        "readonly": true,
        "default": false
      },
      {
        "name": "Logging & Status",
        "readonly": false,
        "default": false
      },
      {
        "name": "SmartEvent Server",
        "readonly": true,
        "default": false
      },
      {
        "name": "User Direct",
        "readonly": true,
        "default": false
      },
      {
        "name": "Provisioning",
        "readonly": true,
        "default": false
      },
      {
        "name": "SmartEvent Correlation Unit",
        "readonly": true,
        "default": false
      }
    ],
    "network-security": [
      {
        "name": "Dynamic Routing",
        "readonly": true,
        "default": true
      },
      {
        "name": "Mobile Access",
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
        "name": "Content Awareness",
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
      },
      {
        "name": "Data Loss Protection",
        "readonly": false,
        "default": false
      },
      {
        "name": "QoS",
        "readonly": false,
        "default": false
      },
      {
        "name": "Policy Server",
        "readonly": true,
        "default": false
      },
      {
        "name": "Application Control",
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
        "name": "Monitoring",
        "readonly": false,
        "default": false
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
      "autonomous": [
        {
          "name": "Sanitization (CDR)",
          "readonly": false,
          "default": true
        },
        {
          "name": "C&C Protection",
          "readonly": false,
          "default": true
        },
        {
          "name": "Threat Cloud",
          "readonly": false,
          "default": true
        },
        {
          "name": "Zero Phishing",
          "readonly": false,
          "default": true
        },
        {
          "name": "File & URL Reputation",
          "readonly": false,
          "default": true
        },
        {
          "name": "Sandbox",
          "readonly": false,
          "default": true
        },
        {
          "name": "IPS Protections",
          "readonly": false,
          "default": true
        }
      ]
    }
  },
  "supported-hardware": {
    "hardware": [
      "2200 Appliance",
      "3000 Appliances",
      "4000 Appliances",
      "5000 Appliances",
      "6000 Appliances",
      "7000 Appliances",
      "12000 Appliances",
      "13000 Appliances",
      "15000 Appliances",
      "16000 Appliances",
      "21000 Appliances",
      "23000 Appliances",
      "26000 Appliances",
      "28000 Appliances",
      "QLS250 Quantum LightSpeed",
      "QLS450 Quantum LightSpeed",
      "QLS650 Quantum LightSpeed",
      "QLS800 Quantum LightSpeed",
      "MLS200 Maestro LightSpeed",
      "MLS400 Maestro LightSpeed",
      "Maestro",
      "CloudGuard IaaS",
      "CloudGuard for NSX",
      "Open Server",
      "Smart-1"
    ],
    "default": "Open Server"
  }
}
```
