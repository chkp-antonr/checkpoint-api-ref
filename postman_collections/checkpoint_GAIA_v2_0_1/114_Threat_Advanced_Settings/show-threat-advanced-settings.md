# show-threat-advanced-settings

**Collection:** Web API (version 2.0.1) > 114 Threat Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-threat-advanced-settings`

## Description

Showing Threat Advanced Settings

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

### Example 1: show-threat-advanced-settings
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
    "lock": "locked by other session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1646644958102,
      "iso-8601": "2022-03-07T11:22+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1646644958102,
      "iso-8601": "2022-03-07T11:22+0200"
    },
    "creator": "System",
    "locking-admin": "aa",
    "locking-session-id": "befdfbc0-0781-44b5-a33d-1dd5a1cc60d9"
  },
  "read-only": true,
  "resource-classification": {
    "mode": "hold",
    "web-service-fail-mode": "block connections"
  },
  "internal-error-fail-mode": "allow connections",
  "session-unification-timeout": 600,
  "feed-retrieving-interval": "00:05",
  "httpi-non-standard-ports": true
}
```
