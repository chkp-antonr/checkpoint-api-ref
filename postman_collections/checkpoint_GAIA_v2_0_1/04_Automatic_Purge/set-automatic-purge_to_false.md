# set-automatic-purge to false

**Collection:** Web API (version 2.0.1) > 04 Automatic Purge
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-automatic-purge`

## Description

Cancel Scheduled Automatic Purge

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "enabled": false
}
```

## Example Responses

### Example 1: set-automatic-purge to false
**Status:** `200 OK`

**Body:**
```javascript
{
  "enabled": false,
  "keep-sessions-by-count": false,
  "keep-sessions-by-days": false
}
```
