# show-sync-with-user-center

**Collection:** Web API (version 2.0.1) > 155 Sync With User Center
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-sync-with-user-center`

## Description

Show sync with user center.

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

### Example 1: show-sync-with-user-center
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a5be5dd0-5c65-406f-b125-237d4f046b65",
  "type": "SyncUcScheduledEvent",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1753281998621,
      "iso-8601": "2025-07-23T17:46+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1728954884344,
      "iso-8601": "2024-10-15T04:14+0300"
    },
    "creator": "System"
  },
  "enabled": false
}
```
