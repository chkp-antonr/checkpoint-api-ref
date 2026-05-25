# show-access-rulebase

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-access-rulebase`

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
  "use-object-dictionary": true
}
```

## Example Responses

### Example 1: show-access-rulebase
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "name": "Network",
  "uid": "21127e7c-d19b-4c65-b9c3-8e20e66ea1ae",
  "rulebase": [
    {
      "from": 1,
      "to": 1,
      "rulebase": [
        {
          "uid": "cb20e1cc-0343-4e22-a6bb-30b92e97675c",
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
              "posix": 1445504073840,
              "iso-8601": "2015-10-22T11:54+0300"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1445245489542,
              "iso-8601": "2015-10-19T12:04+0300"
            },
            "creator": "aa"
          },
          "install-on": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "none",
              "xmlType": "Global",
              "uid": "6c488338-8eec-4103-ad21-cd461ac2c476",
              "folder": {
                "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
                "name": "Check Point Settings"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Policy Targets",
              "icon": "General/globalsAny",
              "comments": "The policy target gateways"
            }
          ],
          "name": "Rule1",
          "source": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "red",
              "xmlType": "dynamic-object",
              "uid": "fe9b9103-f1c0-499e-985a-d15ccc7ebaab",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711955857,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711955857,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "CPDShield",
              "icon": "NetworkObjects/dynamicObject",
              "comments": "DSHIELD IP blocklist",
              "display-name": ""
            }
          ],
          "source-negate": false,
          "destination": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "destination-negate": false,
          "service": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "service-negate": false,
          "vpn": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "action": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "RulebaseAction",
            "uid": "6c488338-8eec-4103-ad21-cd461ac2c473",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "Drop",
            "icon": "Actions/actionsDrop",
            "comments": "Drop",
            "display-name": "Drop"
          },
          "action-settings": {
            "enable-identity-captive-portal": false
          },
          "data": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "data-negate": false,
          "data-direction": "any",
          "track": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "Track",
            "uid": "29e53e3d-23bf-48fe-b6b1-d59bd88036f9",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "None",
            "icon": "General/globalsNone",
            "comments": "Extended Log used in Application Site rulebase"
          },
          "track-alert": "none",
          "time": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "custom-fields": {
            "field-1": "",
            "field-2": "",
            "field-3": ""
          },
          "rule-number": 1,
          "type": "rule"
        }
      ],
      "name": "Section1",
      "uid": "c53d4aac-6c1b-4c75-aea2-3105612c302c",
      "type": "section"
    },
    {
      "from": 2,
      "to": 3,
      "rulebase": [
        {
          "uid": "ae36ddad-4a82-456b-93aa-a97320ff47df",
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
              "posix": 1445504129222,
              "iso-8601": "2015-10-22T11:55+0300"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1445504082424,
              "iso-8601": "2015-10-22T11:54+0300"
            },
            "creator": "aa"
          },
          "install-on": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "none",
              "xmlType": "Global",
              "uid": "6c488338-8eec-4103-ad21-cd461ac2c476",
              "folder": {
                "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
                "name": "Check Point Settings"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Policy Targets",
              "icon": "General/globalsAny",
              "comments": "The policy target gateways"
            }
          ],
          "name": "Rule2",
          "source": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "source-negate": false,
          "destination": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "red",
              "xmlType": "dynamic-object",
              "uid": "fe9b9103-f1c0-499e-985a-d15ccc7ebaab",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711955857,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711955857,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "CPDShield",
              "icon": "NetworkObjects/dynamicObject",
              "comments": "DSHIELD IP blocklist",
              "display-name": ""
            }
          ],
          "destination-negate": false,
          "service": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "service-negate": false,
          "vpn": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "action": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "RulebaseAction",
            "uid": "6c488338-8eec-4103-ad21-cd461ac2c473",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "Drop",
            "icon": "Actions/actionsDrop",
            "comments": "Drop",
            "display-name": "Drop"
          },
          "action-settings": {
            "enable-identity-captive-portal": false
          },
          "data": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "data-negate": false,
          "data-direction": "any",
          "track": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "Track",
            "uid": "29e53e3d-23bf-48fe-b6b1-d59bd88036f9",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "None",
            "icon": "General/globalsNone",
            "comments": "Extended Log used in Application Site rulebase"
          },
          "track-alert": "none",
          "time": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "custom-fields": {
            "field-1": "",
            "field-2": "",
            "field-3": ""
          },
          "rule-number": 2,
          "type": "rule"
        },
        {
          "uid": "88e09e3a-a935-4b33-94f4-1f62b2d8b78a",
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
              "posix": 1445504138184,
              "iso-8601": "2015-10-22T11:55+0300"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1445504082982,
              "iso-8601": "2015-10-22T11:54+0300"
            },
            "creator": "aa"
          },
          "install-on": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "none",
              "xmlType": "Global",
              "uid": "6c488338-8eec-4103-ad21-cd461ac2c476",
              "folder": {
                "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
                "name": "Check Point Settings"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711969368,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Policy Targets",
              "icon": "General/globalsAny",
              "comments": "The policy target gateways"
            }
          ],
          "name": "Rule3",
          "source": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "security-zone",
              "uid": "e8131db2-8388-42a5-924a-82de32db20f7",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711955871,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711955871,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "InternalZone",
              "icon": "NetworkObjects/zone",
              "comments": "",
              "display-name": ""
            }
          ],
          "source-negate": false,
          "destination": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "dynamic-object",
              "uid": "cac127fb-24f5-4079-9404-be5c00d11393",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711955855,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711955855,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "AuxiliaryNet",
              "icon": "NetworkObjects/dynamicObject",
              "comments": "",
              "display-name": ""
            }
          ],
          "destination-negate": false,
          "service": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "service-negate": false,
          "vpn": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "action": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "RulebaseAction",
            "uid": "6c488338-8eec-4103-ad21-cd461ac2c473",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969650,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "Drop",
            "icon": "Actions/actionsDrop",
            "comments": "Drop",
            "display-name": "Drop"
          },
          "action-settings": {
            "enable-identity-captive-portal": false
          },
          "data": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "data-negate": false,
          "data-direction": "any",
          "track": {
            "domainId": {
              "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
              "name": "Check Point Data",
              "type": "data domain"
            },
            "color": "none",
            "xmlType": "Track",
            "uid": "29e53e3d-23bf-48fe-b6b1-d59bd88036f9",
            "folder": {
              "uid": "a7a569db-cd04-4f1c-bc8d-94dbfc22b150",
              "name": "Check Point Settings"
            },
            "meta-info": {
              "validation-state": "ok",
              "last-modify-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "last-modifier": "System",
              "creation-time": {
                "posix": 1444711969451,
                "iso-8601": "2015-10-13T07:52+0300"
              },
              "creator": "System"
            },
            "tags": [],
            "name": "None",
            "icon": "General/globalsNone",
            "comments": "Extended Log used in Application Site rulebase"
          },
          "track-alert": "none",
          "time": [
            {
              "domainId": {
                "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
                "name": "Check Point Data",
                "type": "data domain"
              },
              "color": "black",
              "xmlType": "CpmiAnyObject",
              "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30",
              "folder": {
                "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39b",
                "name": "Global Objects"
              },
              "meta-info": {
                "validation-state": "ok",
                "last-modify-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "last-modifier": "System",
                "creation-time": {
                  "posix": 1444711951589,
                  "iso-8601": "2015-10-13T07:52+0300"
                },
                "creator": "System"
              },
              "tags": [],
              "name": "Any",
              "icon": "General/globalsAny",
              "display-name": ""
            }
          ],
          "custom-fields": {
            "field-1": "",
            "field-2": "",
            "field-3": ""
          },
          "rule-number": 3,
          "type": "rule"
        }
      ],
      "name": "Seciton2",
      "uid": "58a00921-65a7-4258-9182-2340a203e4ee",
      "type": "section"
    }
  ]
}
```
