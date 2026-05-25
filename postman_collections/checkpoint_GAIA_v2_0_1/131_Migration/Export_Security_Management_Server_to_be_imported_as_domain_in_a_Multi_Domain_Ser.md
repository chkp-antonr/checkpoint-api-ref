# Export Security Management Server to be imported as domain in a Multi Domain Server

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/export-management`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/var/log/smc_exported.tgz",
  "is-smc-to-mds": true
}
```

## Example Responses

### Example 1: Export Security Management Server to be imported as domain in a Multi Domain Server
**Status:** `200 OK`
