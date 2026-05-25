# set-threat-advanced-settings (with custom settings)

**Collection:** Web API (version 2.1) > 125 Threat Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-advanced-settings`

## Description

Setting Threat Advanced Settings with custom settings of resources classification

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "resource-classification.mode": "custom",
  "resource-classification.custom-settings.anti-bot": "hold",
  "resource-classification.custom-settings.anti-virus": "background",
  "internal-error-fail-mode": "allow connections",
  "log-unification-timeout": 600,
  "feed-retrieving-interval": "00:05",
  "httpi-non-standard-ports": true
}
```

## Example Responses

### Example 1: set-threat-advanced-settings (with custom settings)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1a080415-3a16-4e2c-8f16-912bcb93aa91",
  "type": "threat-advanced-settings",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1648121778409,
      "iso-8601": "2022-03-24T13:36+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1646644958102,
      "iso-8601": "2022-03-07T11:22+0200"
    },
    "creator": "System"
  },
  "read-only": true,
  "resource-classification": {
    "mode": "custom",
    "custom-settings": {
      "anti-bot": "hold",
      "anti-virus": "background",
      "zero-phishing": "background"
    },
    "web-service-fail-mode": "allow connections"
  },
  "internal-error-fail-mode": "allow connections",
  "log-unification-timeout": 600,
  "feed-retrieving-interval": "00:05",
  "httpi-non-standard-ports": true
}
```
