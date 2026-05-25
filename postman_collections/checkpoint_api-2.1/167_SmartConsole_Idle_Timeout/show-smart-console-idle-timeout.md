# show-smart-console-idle-timeout

**Collection:** Web API (version 2.1) > 167 SmartConsole Idle Timeout
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-smart-console-idle-timeout`

## Description

Retrieve Smart Console idle timeout settings.

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

### Example 1: show-smart-console-idle-timeout
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4ede4f13-58f3-47ed-9f6c-d16c6c77c232",
  "type": "smart-console-idle-timeout",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1738765942650,
      "iso-8601": "2025-02-05T16:32+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1738588308540,
      "iso-8601": "2025-02-03T15:11+0200"
    },
    "creator": "System"
  },
  "enabled": true,
  "timeout-duration": 30
}
```
