# show-app-control-status

**Collection:** Web API (version 2.0.1) > 78 Application Control & URL Filtering Update
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-app-control-status`

## Description

Display Application Control & URL Filtering status

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

### Example 1: show-app-control-status
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4a716234-983d-463c-a1e7-410607a66c11",
  "type": "app-control-status",
  "domain": {
    "uid": "8bf4ac51-2df7-40e1-9bce-bedbedbedbed",
    "name": "APPI Data",
    "domain-type": "data domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1738588386303,
      "iso-8601": "2025-02-03T15:13+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1738588325536,
      "iso-8601": "2025-02-03T15:12+0200"
    },
    "creator": "System"
  },
  "last-updated": {
    "posix": 1738588386303,
    "iso-8601": "2025-02-03T15:13+0200"
  },
  "installed-version": "0",
  "installed-version-creation-time": {
    "posix": 1593982800000,
    "iso-8601": "2020-07-06T00:00+0300"
  }
}
```
