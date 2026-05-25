# clone-gaia-best-practice

**Collection:** Web API (version 2.1) > 70 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-gaia-best-practice`

## Description

Clone existing Gaia Best Practice.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Make sure that the network access via Telnet is disabled."
}
```

## Example Responses

### Example 1: clone-gaia-best-practice
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3968b5ef-b380-42a6-8818-804ae3599d1f",
  "name": "Make sure that the network access via Telnet is disabled.",
  "type": "Gaia OS",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747412030486,
      "iso-8601": "2025-05-16T19:13+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1747412030486,
      "iso-8601": "2025-05-16T19:13+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "read-only": true,
  "best-practice-id": "OS001",
  "description": "This Gaia Best Practice makes sure that the network access, via Telnet, is disabled.",
  "action-item": "Validate that the Telnet settings are disabled on the configuration set on the GAIA OS.",
  "status": "N/A",
  "expected-output-base64": "U3VjY2Vzcw==",
  "practice-script-base64": "IyEvYmluL2Jhc2gKCnRlbG5ldF9vZmY9JChjbGlzaCAtYyAic2hvdyBjb25maWd1cmF0aW9uIiB8IGdyZXAgInNldCBuZXQtYWNjZXNzIHRlbG5ldCIgfCBncmVwICJvZmYiKQppZiBbICEgLXogIiR0ZWxuZXRfb2ZmIiBdOyB0aGVuCgllY2hvIFN1Y2Nlc3MKZWxzZQoJZWNobyBGYWlsCmZp",
  "user-defined": true
}
```
