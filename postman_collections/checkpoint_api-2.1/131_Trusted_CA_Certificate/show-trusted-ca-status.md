# show-trusted-ca-status

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-trusted-ca-status`

## Description

Show trusted CA status

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

### Example 1: show-trusted-ca-status
**Status:** `200 OK`

**Body:**
```javascript
{
  "last-updated": {
    "posix": 1744066808000,
    "iso-8601": "2025-04-08T02:00+0300"
  },
  "installed-version": "3.6",
  "latest-version": "3.6",
  "update-available": false,
  "connection-status": "online",
  "latest-version-creation-time": {
    "posix": 1739656800000,
    "iso-8601": "2025-02-16T00:00+0200"
  },
  "last-checked": {
    "posix": 1746432013968,
    "iso-8601": "2025-05-05T11:00+0300"
  }
}
```
