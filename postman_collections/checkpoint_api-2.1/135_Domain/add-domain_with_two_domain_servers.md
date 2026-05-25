# add-domain with two domain servers

**Collection:** Web API (version 2.1) > 135 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-domain`

## Description

Create a domain with a multi domain and a log server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain1",
  "servers": [
    {
      "ip-address": "192.0.2.1",
      "name": "domain1_ManagementServer_1",
      "multi-domain-server": "MDM_Server",
      "type": "management server"
    },
    {
      "ip-address": "192.0.2.2",
      "name": "domain1_Log_Server_1",
      "multi-domain-server": "Log_Server",
      "active": false,
      "type": "log server"
    }
  ]
}
```

## Example Responses

### Example 1: add-domain with two domain servers
**Status:** `200 OK`
