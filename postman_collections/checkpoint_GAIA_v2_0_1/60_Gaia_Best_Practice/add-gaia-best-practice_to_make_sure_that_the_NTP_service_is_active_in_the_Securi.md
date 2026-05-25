# add-gaia-best-practice to make sure that the NTP service is active in the Security Gateway.

**Collection:** Web API (version 2.0.1) > 60 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-gaia-best-practice`

## Description

Add a new Gaia Best Practice (using a script in Base64) to make sure that the NTP service is active in the Security Gateway.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Make sure that the NTP service is active in the Security Gateway.",
  "description": "This Gaia Best Practice checks that the NTP service is turned On in the Security Gateway.",
  "action-item": "Verify that the NTP settings are enabled.",
  "expected-output-text": "Secure",
  "practice-script-base64": "IyEvYmluL2Jhc2gKCkNQTDE9JChjbGlzaCAtaWMgJ3Nob3cgY29uZmlndXJhdGlvbicgfCBncmVwICdudHAgYWN0aXZlJyB8IGF3ayAne3ByaW50ICQ0fScgKQoKaWYgW1sgLXogJENQTDEgXV07IHRoZW4KCQlleGl0IDEgCmZpCgppZiBbWyAkQ1BMMSA9PSAib24iIF1dOyB0aGVuIAoJCWVjaG8gJ1NlY3VyZScgCmVsc2UgCgkJZWNobyAnUG9vcicgCmZpIA=="
}
```

## Example Responses

### Example 1: add-gaia-best-practice to make sure that the NTP service is active in the Security Gateway.
**Status:** `200 OK`

**Body:**
```javascript
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
}
```
