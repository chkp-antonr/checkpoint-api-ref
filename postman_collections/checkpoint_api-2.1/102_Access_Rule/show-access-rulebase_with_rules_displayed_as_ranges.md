# show-access-rulebase with rules displayed as ranges

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-access-rulebase`

## Description

Shows the Access Rules with their members displayed as ranges, and not as Check Point Objects. This is limited to maximum 20 rules at a time.

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
  "show-as-ranges": "true"
}
```

## Example Responses

### Example 1: show-access-rulebase with rules displayed as ranges
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7f7308f0-7540-4631-832c-503de7b27c3d",
  "name": "Network",
  "from": 1,
  "to": 1,
  "total": 1,
  "rulebase": [
    {
      "uid": "0f83bd2b-7d7c-4063-920b-c160779437e1",
      "name": "Stealth Rules",
      "type": "access-section",
      "from": 1,
      "to": 1,
      "rulebase": [
        {
          "uid": "36e2e7fd-e2af-4b6c-8692-6aa77f8f4913",
          "name": "Admin access to the Gateways",
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
              "posix": 1527405735252,
              "iso-8601": "2018-05-27T10:22+0300"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1527405608448,
              "iso-8601": "2018-05-27T10:20+0300"
            },
            "creator": "aa"
          },
          "install-on": [
            "6c488338-8eec-4103-ad21-cd461ac2c476"
          ],
          "source-ranges": {
            "ipv4": [
              {
                "start": "192.168.200.133",
                "end": "192.168.200.133"
              },
              {
                "start": "192.168.20.132",
                "end": "192.168.20.132"
              },
              {
                "start": "192.168.200.131",
                "end": "192.168.200.131"
              }
            ],
            "ipv6": [],
            "others": [],
            "excluded-others": []
          },
          "destination-ranges": {
            "ipv4": [
              {
                "start": "172.23.26.177",
                "end": "172.23.26.177"
              }
            ],
            "ipv6": [],
            "others": [],
            "excluded-others": []
          },
          "service-ranges": {
            "tcp": [
              {
                "start": "22",
                "end": "22"
              }
            ],
            "udp": [],
            "others": [
              "97aeb40f-9aea-11d5-bd16-0090272ccb30",
              "97aeb40a-9aea-11d5-bd16-0090272ccb30",
              "97aeb40d-9aea-11d5-bd16-0090272ccb30",
              "97aeb411-9aea-11d5-bd16-0090272ccb30"
            ],
            "excluded-others": []
          },
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
          "time": [
            "97aeb369-9aea-11d5-bd16-0090272ccb30"
          ],
          "custom-fields": {
            "field-1": "",
            "field-2": "",
            "field-3": ""
          },
          "rule-number": 1,
          "track": {
            "type": "598ead32-aa42-4615-90ed-f51a5928d41d",
            "per-session": false,
            "per-connection": true,
            "accounting": false,
            "alert": "none"
          }
        }
      ]
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
      "uid": "ac661e37-6f77-0a41-97aa-59d8f5fb585e",
      "name": "halo-270-smx-take-29",
      "type": "CpmiHostCkp",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "598ead32-aa42-4615-90ed-f51a5928d41d",
      "name": "Log",
      "type": "Track",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "bfacd5ee-86bb-4da5-8366-b5de4a753229",
      "name": "Manage-Services",
      "type": "service-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
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
    },
    {
      "uid": "7727af92-2ee9-4afc-965e-5411cb3129e3",
      "name": "Support-Specialists",
      "type": "group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
