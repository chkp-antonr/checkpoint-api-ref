# show-best-practices

**Collection:** Web API (version 2.1) > 69 Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-best-practices`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": "5"
}
```

## Example Responses

### Example 1: show-best-practices
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 5,
  "total": 264,
  "objects": [
    {
      "uid": "097f15a8-6186-4bea-9cfb-877aa9425f47",
      "name": "Check that 'Clean up Rule' is defined in Access Policy",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747861265056,
          "iso-8601": "2025-05-22T00:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665908508,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "false"
      },
      "read-only": false,
      "best-practice-id": "FW101",
      "description": "This check whether the 'Clean up Rule' is the last row listed in the Access Policy Rule Base and is applied to all Gateways. A 'Clean up Rule' is defined as: Source= Any; Destination= Any; VPN= Any Traffic; Service= Any; Action= Drop; Track= Not None; Install On: all network objects that linked to the Policy, Time= Any,",
      "action-item": "The 'Clean up Rule' in the Access Policy Rule Base needs to be defined as follows: Source = Any; Destination = Any; VPN = Any Traffic; Service = Any; Action = Drop; Track = Not None; Install On: all network objects that linked to the Policy, Time = Any. Note that the 'Clean up Rule' must be the last row listed in the Access Policy Rule Base. The purpose of the check is to ensure that on each Gateway a clean up rule is enforced. This is enforced by ensuring all policy packages include a clean up rule but at the end of the policy.",
      "status": "medium",
      "blade": "firewall",
      "user-defined": false,
      "relevant-objects": {
        "relevant-objects-type": "access-rule",
        "access-rules-info": [
          {
            "policy-name": "Standard",
            "layer-name": "Network",
            "layer-uid": "bc2c2a63-ef09-4e4f-a219-3bda9c621109",
            "rule-indexes": "",
            "status": "medium",
            "enabled": true
          }
        ]
      },
      "active": true
    },
    {
      "uid": "222370d0-4834-4c5b-8389-dc3f5bee90a6",
      "name": "Check that 'Encrypt DNS traffic' is selected in the Remote Access settings in the Global Properties",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747861265322,
          "iso-8601": "2025-05-22T00:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665910045,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "read-only": false,
      "best-practice-id": "VPN122",
      "description": "This checks the Remote Access settings in the Global Properties to ensure that 'Encrypt DNS traffic' is selected",
      "action-item": "The 'Encrypt DNS traffic' option should be selected in the Remote Access settings in the Global Properties",
      "status": "secure",
      "blade": "ipsec-vpn",
      "user-defined": false,
      "active": true
    },
    {
      "uid": "68758daf-04ef-4a7b-84de-a94dc8e3cf4b",
      "name": "Check the Simultaneous Login setting within Remote Access",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747861267119,
          "iso-8601": "2025-05-22T00:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665910105,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "read-only": false,
      "best-practice-id": "VPN128",
      "description": "This checks the Simultaneous Login setting to ensure that 'User is only allowed single login' is selected",
      "action-item": "In SmartConsole, click Menu - 'Global properties'.  Click the 'Remote Access' page. In the 'Simultaneous Login' section, select 'User is only allowed single login'.",
      "status": "secure",
      "blade": "ipsec-vpn",
      "user-defined": false,
      "active": true
    },
    {
      "uid": "9221b09e-7cb0-4ffc-a0ae-2a387876cbb5",
      "name": "Check the Endpoint Connect password caching settings in the Global Properties.",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747861267574,
          "iso-8601": "2025-05-22T00:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665910115,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "read-only": false,
      "best-practice-id": "VPN132",
      "description": "This checks the Endpoint Connect password caching settings in the Global Properties under Remote Access. Password caching should either be set to 'No', or, if it set to 'Yes', the password should not be cached for more than 1,440 minutes. If 'Configured on Endpoint Client' has been selected, the best practice will be set to NA.",
      "action-item": "Password Caching for Endpoint Connect is defined in the Global Properties under Remote Access. Password caching should either be set to 'No', or if it is set to Yes, then the password should not be cached for more than 1,440 minutes. If 'Configured on Endpoint Client' has been selected, the best practice will be set as NA.",
      "status": "secure",
      "blade": "ipsec-vpn",
      "user-defined": false,
      "active": true
    },
    {
      "uid": "ab535389-28e3-4880-ad3b-9a379aece834",
      "name": "Check the Endpoint Connect 'Re-authenticate user' settings in the Global Properties",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747861267862,
          "iso-8601": "2025-05-22T00:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665910125,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "read-only": false,
      "best-practice-id": "VPN133",
      "description": "This checks the Endpoint Connect 'Re-authenticate user' settings in the Global Properties under Remote Access. Re-authentication should be set at 120 minutes or less.",
      "action-item": "The 'Re-authenticate user' settings for Endpoint Connect is defined in the Global Properties under Remote Access. Re-authentication should be set at 120 minutes or less. The scoring parameters are as follows: Poor (more than 480 minutes), Medium (between 301 minutes and 480 minutes), Good (between 121 minutes and 300 minutes), and Secure (120 minutes or less)",
      "status": "medium",
      "blade": "ipsec-vpn",
      "user-defined": false,
      "active": true
    }
  ]
}
```
