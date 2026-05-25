# show-gaia-best-practice

**Collection:** Web API (version 2.0.1) > 60 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-gaia-best-practices`

## Description

Show all Gaia Best Practices.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-gaia-best-practice
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 5,
  "total": 5,
  "objects": [
    {
      "uid": "4b4cc5fb-ed56-412b-937a-37a9f2ecbd68",
      "name": "Check that a Secondary DNS Server is defined",
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
          "posix": 1605526391000,
          "iso-8601": "2020-11-16T13:33+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1605005977000,
          "iso-8601": "2020-11-10T12:59+0200"
        }
      },
      "read-only": true,
      "best-practice-id": "OS120",
      "description": "This checks that a secondary DNS server is correctly defined. This should be a host running a DNS server.",
      "action-item": "Add or modify the secondary DNS server. This should be a host running a DNS server.",
      "status": "N/A",
      "expected-output-base64": "N/A",
      "practice-script-base64": "N/A",
      "user-defined": false
    },
    {
      "uid": "7f8dd590-13bd-4ca0-858d-98edda833b19",
      "name": "Check that a DNS Suffix is configured",
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
          "posix": 1605526391000,
          "iso-8601": "2020-11-16T13:33+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1605005977000,
          "iso-8601": "2020-11-10T12:59+0200"
        }
      },
      "read-only": true,
      "best-practice-id": "OS118",
      "description": "This checks that a correctly configured DNS suffix is defined. By default, the DNS suffix should be the local domain name. The domain suffix must be made up of alphanumeric characters separated by period, e.g. 'example.com'.",
      "action-item": "The DNS Suffix must be correctly defined. The domain suffix must be made up of alphanumeric characters separated by period, e.g. 'example.com'.",
      "status": "N/A",
      "expected-output-base64": "N/A",
      "practice-script-base64": "N/A",
      "user-defined": false
    },
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
    },
    {
      "uid": "af439463-8370-416b-8bab-55e702a37274",
      "name": "Make sure that the NTP service is active in the Security Gateway.",
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
      "best-practice-id": "OS002",
      "description": "This Gaia Best Practice checks that the NTP service is turned On in the Security Gateway.",
      "action-item": "Verify that the NTP settings are enabled.",
      "status": "N/A",
      "expected-output-base64": "U2VjdXJl",
      "practice-script-base64": "IyEvYmluL2Jhc2gKCkNQTDE9JChjbGlzaCAtaWMgJ3Nob3cgY29uZmlndXJhdGlvbicgfCBncmVwICdudHAgYWN0aXZlJyB8IGF3ayAne3ByaW50ICQ0fScgKQoKaWYgW1sgLXogJENQTDEgXV07IHRoZW4KCQlleGl0IDEgCmZpCgppZiBbWyAkQ1BMMSA9PSAib24iIF1dOyB0aGVuIAoJCWVjaG8gJ1NlY3VyZScgCmVsc2UgCgkJZWNobyAnUG9vcicgCmZpIA==",
      "user-defined": true
    },
    {
      "uid": "af439463-8370-416b-8bab-55e702a37274",
      "name": "New Best Practice",
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
      "best-practice-id": "OS003",
      "description": "This Best Practice will be used for testing purposes.",
      "action-item": "The script must output Success for this Best Practice to be in status Secure.",
      "status": "N/A",
      "expected-output-base64": "U3VjY2Vzcw==",
      "practice-script-base64": "IyEvYmluL2Jhc2gKZWNobyAiU3VjY2VzcyIKZXhpdCAw",
      "user-defined": true
    }
  ]
}
```
