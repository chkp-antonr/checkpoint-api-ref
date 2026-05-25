# show-threat-rule-exception-rulebase

**Collection:** Web API (version 2.1) > 114 Threat Exception
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-threat-rule-exception-rulebase`

## Description

show threat exception rulebase of a threat rule

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
  "rule-number": 1
}
```

## Example Responses

### Example 1: show-threat-rule-exception-rulebase
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "36d13425-3be6-427f-a7bd-7ddec5248cc1",
  "name": "ThreatStandardSubRulebase",
  "rulebase": [
    {
      "uid": "685ebbb2-8d9d-4908-9af4-77a823e22e76",
      "name": "Global Exceptions",
      "type": "threat-section",
      "rulebase": []
    }
  ],
  "total": 0
}
```
