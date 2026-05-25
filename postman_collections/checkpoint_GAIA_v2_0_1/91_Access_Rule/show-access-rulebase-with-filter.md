# show-access-rulebase-with-filter

**Collection:** Web API (version 2.0.1) > 91 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-access-rulebase`

## Description

Shows the entire Access Rules Rulebase.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "offset": 0,
  "limit": 20,
  "name": "Network",
  "details-level": "standard",
  "use-object-dictionary": true,
  "filter": "CPDShield"
}
```

## Example Responses

### Example 1: show-access-rulebase-with-filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "aa7b850a-db90-4e5e-91c1-cb21bced1a93",
  "name": "Network",
  "from": 1,
  "to": 1,
  "total": 1,
  "rulebase": [
    {
      "uid": "76b830c8-e43f-4c9a-9722-8353829ff7b1",
      "name": "Rule1",
      "type": "access-rule",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "enabled": true,
      "comments": "",
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1482658663305,
          "iso-8601": "2016-12-25T11:37+0200"
        },
        "last-modifier": "aa",
        "creation-time": {
          "posix": 1482150758417,
          "iso-8601": "2016-12-19T14:32+0200"
        },
        "creator": "aa"
      },
      "install-on": [
        "6c488338-8eec-4103-ad21-cd461ac2c476"
      ],
      "source": [
        "237a4cbc-7fb6-4d50-872a-4904468271c4"
      ],
      "source-negate": false,
      "destination": [
        "97aeb369-9aea-11d5-bd16-0090272ccb30"
      ],
      "destination-negate": false,
      "service": [
        "97aeb369-9aea-11d5-bd16-0090272ccb30"
      ],
      "service-negate": false,
      "vpn": [
        "97aeb369-9aea-11d5-bd16-0090272ccb30"
      ],
      "action": "6c488338-8eec-4103-ad21-cd461ac2c472",
      "action-settings": {
        "enable-identity-captive-portal": false
      },
      "content": [
        "97aeb369-9aea-11d5-bd16-0090272ccb30"
      ],
      "content-negate": false,
      "content-direction": "any",
      "track": "29e53e3d-23bf-48fe-b6b1-d59bd88036f9",
      "track-alert": "none",
      "time": [
        "97aeb369-9aea-11d5-bd16-0090272ccb30"
      ],
      "custom-fields": {
        "field-1": "",
        "field-2": "",
        "field-3": ""
      },
      "rule-number": 1
    }
  ],
  "objects-dictionary": [
    {
      "uid": "6c488338-8eec-4103-ad21-cd461ac2c472",
      "name": "Accept",
      "type": "RulebaseAction",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
      "name": "Any",
      "type": "CpmiAnyObject",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "237a4cbc-7fb6-4d50-872a-4904468271c4",
      "name": "ExternalZone",
      "type": "security-zone",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "29e53e3d-23bf-48fe-b6b1-d59bd88036f9",
      "name": "None",
      "type": "Track",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "6c488338-8eec-4103-ad21-cd461ac2c476",
      "name": "Policy Targets",
      "type": "Global",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    }
  ]
}
```
