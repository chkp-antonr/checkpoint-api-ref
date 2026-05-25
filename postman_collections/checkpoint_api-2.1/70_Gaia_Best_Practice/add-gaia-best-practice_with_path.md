# add-gaia-best-practice with path

**Collection:** Web API (version 2.1) > 70 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-gaia-best-practice`

## Description

Add a new Gaia Best Practice using an absolute path to a script file on the Management

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Best Practice",
  "description": "This Best Practice will be used for testing purposes.",
  "action-item": "The script must output Success for this Best Practice to be in status Secure.",
  "expected-output-text": "Success",
  "practice-script-path": "/var/tmp/print_success_script.sh"
}
```

## Example Responses

### Example 1: add-gaia-best-practice with path
**Status:** `200 OK`

**Body:**
```javascript
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
```
