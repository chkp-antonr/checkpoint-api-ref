# set-domain add log server

**Collection:** Web API (version 2.0.1) > 124 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-domain`

## Description

Edit an existing domain, add a log server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain2",
  "servers": {
    "add": {
      "ip-address": "192.0.2.4",
      "name": "domain2_Log_Server_2",
      "multi-domain-server": "Log_Server",
      "type": "log server"
    }
  }
}
```

## Example Responses

### Example 1: set-domain add log server
**Status:** `200 OK`
