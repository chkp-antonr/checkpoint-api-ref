# show-nat-rulebase-with-filter

**Collection:** Web API (version 2.0.1) > 94 NAT Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-nat-rulebase`

## Description

Shows the entire NAT Rules Rulebase.

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
  "limit": 50,
  "details-level": "standard",
  "use-object-dictionary": true,
  "package": "standard",
  "filter": "ssh_version_2"
}
```

## Example Responses

### Example 1: show-nat-rulebase-with-filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "uid": "4862b29a-1753-4d19-9142-6814c7377474",
  "rulebase": [
    {
      "from": 1,
      "to": 2,
      "rulebase": [
        {
          "uid": "86fc210c-9fa4-4cfa-83bb-d6377853dd20",
          "enabled": true,
          "comments": "rule for RND members  RNDNetwork-> RND to Internal Network",
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
              "posix": 1450932209522,
              "iso-8601": "2015-12-24T06:43+0200"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1450932130503,
              "iso-8601": "2015-12-24T06:42+0200"
            },
            "creator": "aa"
          },
          "install-on": [
            "6c488338-8eec-4103-ad21-cd461ac2c476"
          ],
          "auto-generated": false,
          "original-destination": "97aeb369-9aea-11d5-bd16-0090272ccb30",
          "translated-destination": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c",
          "original-source": "97aeb369-9aea-11d5-bd16-0090272ccb30",
          "translated-source": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c",
          "original-service": "cd082d9a-44a6-4cef-a17d-5541029adfb3",
          "translated-service": "cd082d9a-44a6-4cef-a17d-5541029adfb3",
          "method": "static",
          "rule-number": 1,
          "type": "rule"
        },
        {
          "uid": "e47a64af-8af0-4a2f-8f54-5fbdcdc252a5",
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
              "posix": 1451453576971,
              "iso-8601": "2015-12-30T07:32+0200"
            },
            "last-modifier": "aa",
            "creation-time": {
              "posix": 1451453557603,
              "iso-8601": "2015-12-30T07:32+0200"
            },
            "creator": "aa"
          },
          "install-on": [
            "6c488338-8eec-4103-ad21-cd461ac2c476"
          ],
          "auto-generated": false,
          "original-destination": "97aeb369-9aea-11d5-bd16-0090272ccb30",
          "translated-destination": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c",
          "original-source": "97aeb369-9aea-11d5-bd16-0090272ccb30",
          "translated-source": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c",
          "original-service": "cd082d9a-44a6-4cef-a17d-5541029adfb3",
          "translated-service": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c",
          "method": "static",
          "rule-number": 2,
          "type": "rule"
        }
      ],
      "name": "Manual Lower Rules",
      "uid": "b65894d2-b2ce-435b-ab31-17678c3fee4e",
      "type": "section"
    }
  ],
  "objects-dictionary": [
    {
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "CpmiAnyObject",
      "name": "Any",
      "uid": "97aeb369-9aea-11d5-bd16-0090272ccb30"
    },
    {
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "Global",
      "name": "Original",
      "uid": "85c0f50f-6d8a-4528-88ab-5fb11d8fe16c"
    },
    {
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "Global",
      "name": "Policy Targets",
      "uid": "6c488338-8eec-4103-ad21-cd461ac2c476"
    },
    {
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      },
      "type": "service-tcp",
      "name": "ssh_version_2",
      "uid": "cd082d9a-44a6-4cef-a17d-5541029adfb3"
    }
  ]
}
```
