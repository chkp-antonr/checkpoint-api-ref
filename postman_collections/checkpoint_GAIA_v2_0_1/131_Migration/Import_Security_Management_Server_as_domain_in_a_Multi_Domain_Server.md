# Import Security Management Server as domain in a Multi Domain Server

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/export-management`

## Description

Import Security Management Server into Multi Domain Server. domain-name, domain-server-name and domain-ip-address must be given

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "domain-name": "domain1",
  "domain-server-name": "domain1_Server",
  "domain-ip-address": "192.0.2.1",
  "file-path": "/var/log/smc_exported.tgz"
}
```

## Example Responses

### Example 1: Import Security Management Server as domain in a Multi Domain Server
**Status:** `200 OK`
