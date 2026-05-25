# Export domain from the Multi Domain server

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/export-management`

## Description

Export domain named domain1 into /var/log/domain1_exported.tgz

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
  "file-path": "/var/log/domain1_exported.tgz"
}
```

## Example Responses

### Example 1: Export domain from the Multi Domain server
**Status:** `200 OK`
