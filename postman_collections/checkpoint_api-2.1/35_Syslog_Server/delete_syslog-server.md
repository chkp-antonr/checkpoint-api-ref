# delete syslog-server

**Collection:** Web API (version 2.1) > 35 Syslog Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-syslog-server`

## Description

Deletes syslog server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newSyslogServer"
}
```

## Example Responses

### Example 1: delete syslog-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
