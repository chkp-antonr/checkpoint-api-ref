# show-threat-rulebase

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
  "name": "Threat Prevention",
  "offset": 0,
  "limit": 20,
  "details-level": "standard",
  "use-object-dictionary": false,
  "filter": ""
}
```

## Example Responses

### Example 1: show-threat-rulebase
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "name": "Threat Prevention",
  "uid": "07643e1b-c7fd-4b54-9844-7b8c92135d1e",
  "rulebase": [
    {
      "uid": "e348f8f5-ef7c-4824-9b85-4000ce0df964",
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
          "posix": 1445233508467,
          "iso-8601": "2015-10-19T08:45+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1444909091900,
          "iso-8601": "2015-10-15T14:38+0300"
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
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "protected-scope-negate": false,
      "name": "rule1",
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
        "name": "Recommended_Profile",
        "uid": "44b83c65-e73c-4d63-aa55-4cdcea4a6d4b"
      },
      "exceptions": [
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "name": "abc",
          "uid": "54ed2702-9184-477b-ba35-bb162733f3dc"
        },
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "name": "exception1",
          "uid": "f99f6d59-e018-4bd6-be15-e385b549e79e"
        },
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "name": "exception2",
          "uid": "aa42fa65-5eee-4b3d-a532-e1218e5e9326"
        }
      ],
      "rule-number": 1,
      "type": "rule"
    },
    {
      "uid": "e9a60e1f-845f-4f83-a5aa-27eba8a69e22",
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
          "posix": 1445247340478,
          "iso-8601": "2015-10-19T12:35+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1445247318560,
          "iso-8601": "2015-10-19T12:35+0300"
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
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "protected-scope-negate": false,
      "name": "spy",
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
        "name": "Recommended_Profile",
        "uid": "44b83c65-e73c-4d63-aa55-4cdcea4a6d4b"
      },
      "rule-number": 2,
      "type": "rule"
    },
    {
      "uid": "570df5aa-427c-4090-896e-dc35b1fdbf42",
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
          "posix": 1445438243630,
          "iso-8601": "2015-10-21T17:37+0300"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1445438243630,
          "iso-8601": "2015-10-21T17:37+0300"
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
          "type": "CpmiAnyObject",
          "name": "Any",
          "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
        }
      ],
      "protected-scope-negate": false,
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
        "name": "Recommended_Profile",
        "uid": "44b83c65-e73c-4d63-aa55-4cdcea4a6d4b"
      },
      "exceptions": [
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "uid": "5edf987e-0a83-4fcb-a37f-d71a8e5e9fd5"
        },
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "name": "exception1",
          "uid": "f99f6d59-e018-4bd6-be15-e385b549e79e"
        },
        {
          "domain": {
            "domain-type": "domain",
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User"
          },
          "type": "threat-exception",
          "name": "exception2",
          "uid": "aa42fa65-5eee-4b3d-a532-e1218e5e9326"
        }
      ],
      "rule-number": 3,
      "type": "rule"
    }
  ]
}
```
