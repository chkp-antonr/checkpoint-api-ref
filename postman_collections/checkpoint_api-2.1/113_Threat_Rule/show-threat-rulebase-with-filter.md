# show-threat-rulebase-with-filter

**Collection:** Web API (version 2.1) > 113 Threat Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-threat-rulebase`

## Description

Shows the entire Threat Rules Rulebase.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Standard Threat Prevention",
  "offset": 0,
  "limit": 20,
  "details-level": "standard",
  "use-object-dictionary": false,
  "filter": "WirelessZone"
}
```

## Example Responses

### Example 1: show-threat-rulebase-with-filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "name": "Standard Threat Prevention",
  "uid": "5244d78e-7749-40e2-8604-4d04bc5ee13f",
  "rulebase": [
    {
      "uid": "25af9a7c-f4e5-4cd5-a6a8-f74f19854db0",
      "enabled": true,
      "comments": "",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "read-only": false,
        "last-modify-time": {
          "posix": 1451453598360,
          "iso-8601": "2015-12-30T07:33+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1450930796908,
          "iso-8601": "2015-12-24T06:19+0200"
        },
        "creator": "System"
      },
      "install-on": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "Global",
          "name": "Policy Targets",
          "uid": "6c488338-8eec-4103-ad21-cd461ac2c476"
        }
      ],
      "source": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "source-negate": false,
      "destination": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "destination-negate": false,
      "service": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "service-negate": false,
      "protected-scope": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "security-zone",
          "name": "WirelessZone",
          "uid": "57de3848-3675-48ed-b045-41378f4babb3"
        }
      ],
      "protected-scope-negate": false,
      "name": "Rule 1",
      "track": {
        "domain": {
          "domain-type": "data domain",
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data"
        },
        "type": "Global",
        "name": "Log",
        "uid": "6c488338-8eec-4103-ad21-cd461ac2c477"
      },
      "track-settings": {
        "packet-capture": true
      },
      "action": {
        "domain": {
          "domain-type": "data domain",
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data"
        },
        "type": "CpmiArmadaNewProfile",
        "name": "Optimized",
        "uid": "fa1aa324-a8cc-4dbd-bc04-f31fdb8abf61"
      },
      "rule-number": 1,
      "type": "rule"
    },
    {
      "uid": "8439c5cd-8879-477c-92af-91ea46b54071",
      "enabled": true,
      "comments": "",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "read-only": false,
        "last-modify-time": {
          "posix": 1451453620395,
          "iso-8601": "2015-12-30T07:33+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1451453601902,
          "iso-8601": "2015-12-30T07:33+0200"
        },
        "creator": "aa"
      },
      "install-on": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "Global",
          "name": "Policy Targets",
          "uid": "6c488338-8eec-4103-ad21-cd461ac2c476"
        }
      ],
      "source": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "source-negate": false,
      "destination": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "destination-negate": false,
      "service": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "service-negate": false,
      "protected-scope": [
        {
          "domain": {
            "domain-type": "data domain",
            "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
            "name": "Check Point Data"
          },
          "type": "security-zone",
          "name": "WirelessZone",
          "uid": "57de3848-3675-48ed-b045-41378f4babb3"
        }
      ],
      "protected-scope-negate": false,
      "name": "Rule 3",
      "track": {
        "domain": {
          "domain-type": "data domain",
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data"
        },
        "type": "Global",
        "name": "Log",
        "uid": "6c488338-8eec-4103-ad21-cd461ac2c477"
      },
      "track-settings": {
        "packet-capture": true
      },
      "action": {
        "domain": {
          "domain-type": "data domain",
          "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
          "name": "Check Point Data"
        },
        "type": "CpmiArmadaNewProfile",
        "name": "Optimized",
        "uid": "fa1aa324-a8cc-4dbd-bc04-f31fdb8abf61"
      },
      "rule-number": 2,
      "type": "rule"
    }
  ]
}
```
