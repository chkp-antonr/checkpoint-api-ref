# Export entire Security Management Server or Multi Domain Server

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/export-management`

## Description

Export entire Security Management Server or Multi Domain Server. If version is not specified, export will be taken to current machine's version

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "version": "R81.10",
  "file-path": "/var/log/exported.tgz"
}
```

## Example Responses

### Example 1: Export entire Security Management Server or Multi Domain Server
**Status:** `200 OK`
