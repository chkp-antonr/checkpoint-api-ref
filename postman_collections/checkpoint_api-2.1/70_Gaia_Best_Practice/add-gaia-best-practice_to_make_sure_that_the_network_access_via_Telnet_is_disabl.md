# add-gaia-best-practice to make sure that the network access via Telnet is disabled.

**Collection:** Web API (version 2.1) > 70 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-gaia-best-practice`

## Description

Add a new Gaia Best Practice (using a script in Base64) to make sure that the network access (via Telnet) is disabled.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Make sure that the network access via Telnet is disabled.",
  "description": "This Gaia Best Practice makes sure that the network access, via Telnet, is disabled.",
  "action-item": "Validate that the Telnet settings are disabled on the configuration set on the GAIA OS.",
  "expected-output-text": "Success",
  "practice-script-base64": "IyEvYmluL2Jhc2gKCnRlbG5ldF9vZmY9JChjbGlzaCAtYyAic2hvdyBjb25maWd1cmF0aW9uIiB8IGdyZXAgInNldCBuZXQtYWNjZXNzIHRlbG5ldCIgfCBncmVwICJvZmYiKQppZiBbICEgLXogIiR0ZWxuZXRfb2ZmIiBdOyB0aGVuCgllY2hvIFN1Y2Nlc3MKZWxzZQoJZWNobyBGYWlsCmZp"
}
```

## Example Responses

### Example 1: add-gaia-best-practice to make sure that the network access via Telnet is disabled.
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "af439463-8370-416b-8bab-55e702a37274",
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
      "posix": 1602172277593,
      "iso-8601": "2020-10-08T18:51+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1602172277593,
      "iso-8601": "2020-10-08T18:51+0300"
    },
    "creator": "WEB_API"
  },
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
