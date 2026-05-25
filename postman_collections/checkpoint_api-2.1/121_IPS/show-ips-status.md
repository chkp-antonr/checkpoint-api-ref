# show-ips-status

**Collection:** Web API (version 2.1) > 121 IPS
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-ips-status`

## Description

Show IPS database status

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

### Example 1: show-ips-status
**Status:** `200 OK`

**Body:**
```javascript
{
  "last-updated": {
    "posix": 1444285828000,
    "iso-8601": "2015-10-08T09:30+0300"
  },
  "installed-version": "635155796",
  "installed-version-creation-time": {
    "posix": 1440928800000,
    "iso-8601": "2015-08-30T13:00+0300"
  },
  "update-available": true,
  "latest-version": "635156726",
  "latest-version-creation-time": {
    "posix": 1444276800000,
    "iso-8601": "2015-10-08T07:00+0300"
  }
}
```
