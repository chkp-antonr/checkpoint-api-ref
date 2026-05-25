# show-access-rulebase with filter expand group with exclusion members

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-access-rulebase`

## Description

For a given Group with Exclusion, shows the Access Control Rules that match at least one member of the "include" part and is not a member of the "except" part. In this example, the group-with-exclusion "HR except Managers" contains the "HR" group in "include" parameter and the "Managers" in the "except" parameter. HR-Managers-Server object is a member of both "HR" and "Managers", and therefore rules which contain this object will not be matched. HR-Employees-Server is a member of "HR" and not a member of "Managers" and therefore rules that contain this object will be matched.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Network",
  "filter": "dst:HR",
  "filter-settings": {
    "packet-search-settings": {
      "expand-group-with-exclusion-members": "true"
    },
    "search-mode": "packet"
  }
}
```

## Example Responses

### Example 1: show-access-rulebase with filter expand group with exclusion members
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7f7308f0-7540-4631-832c-503de7b27c3d",
  "name": "Network",
  "from": 1,
  "to": 3,
  "total": 3,
  "rulebase": [
    {
      "uid": "fcb7d62b-b499-4b64-94ae-bfc9f4a0a15a",
      "name": "HR Access",
      "type": "access-section",
      "from": 2,
      "to": 2,
      "rulebase": [
        {
          "uid": "723030ba-a33f-44d7-813d-9afa2b7177fb",
          "type": "access-rule",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "enabled": true,
          "comments": "",
          "meta-info": {
            "lock": "locked by current session",
            "validation-state": "ok",
            "last-modify-time": {
              "posix": 1527523152630,
              "iso-8601": "2018-05-28T18:59+0300"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1527523116888,
              "iso-8601": "2018-05-28T18:58+0300"
            },
            "creator": "aa"
          },
          "install-on": [
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
          ],
          "source": [
            {
              "uid": "c9f1f3dd-fd13-4c18-8145-2c752f1487ef",
              "name": "HR-Recruiters",
              "type": "group",
              "domain": {
                "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
                "name": "SMC User",
                "domain-type": "domain"
              }
            }
          ],
          "source-negate": false,
          "destination": [
            {
              "uid": "04d80be4-1a1f-4802-bba9-c659479cfe47",
              "name": "HR-Employees-Server",
              "type": "host",
              "domain": {
                "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
                "name": "SMC User",
                "domain-type": "domain"
              },
              "ipv4-address": "192.168.200.51"
            }
          ],
          "destination-negate": false,
          "service": [
            {
              "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30",
              "name": "https",
              "type": "service-tcp",
              "domain": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "domain-type": "data domain"
              },
              "port": "443"
            }
          ],
          "service-negate": false,
          "vpn": [
            {
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "name": "Any",
              "type": "CpmiAnyObject",
              "domain": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "domain-type": "data domain"
              }
            }
          ],
          "action": {
            "uid": "6c488338-8eec-4103-ad21-cd461ac2c472",
            "name": "Accept",
            "type": "RulebaseAction",
            "domain": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "domain-type": "data domain"
            }
          },
          "action-settings": {
            "enable-identity-captive-portal": false
          },
          "content": [
            {
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "name": "Any",
              "type": "CpmiAnyObject",
              "domain": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "domain-type": "data domain"
              }
            }
          ],
          "content-negate": false,
          "content-direction": "any",
          "time": [
            {
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "name": "Any",
              "type": "CpmiAnyObject",
              "domain": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "domain-type": "data domain"
              }
            }
          ],
          "custom-fields": {
            "field-1": "",
            "field-2": "",
            "field-3": ""
          },
          "track": {
            "type": {
              "uid": "598ead32-aa42-4615-90ed-f51a5928d41d",
              "name": "Log",
              "type": "Track",
              "domain": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "domain-type": "data domain"
              }
            },
            "per-session": false,
            "per-connection": true,
            "accounting": false,
            "alert": "none"
          }
        }
      ]
    }
  ]
}
```
