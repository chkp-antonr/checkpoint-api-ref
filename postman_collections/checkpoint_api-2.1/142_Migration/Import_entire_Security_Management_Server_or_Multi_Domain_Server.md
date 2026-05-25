# Import entire Security Management Server or Multi Domain Server

**Collection:** Web API (version 2.1) > 142 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.1/import-management`

## Description

Import entire Security Management Server or Multi Domain Server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/var/log/exported.tgz"
}
```

## Example Responses

### Example 1: Import entire Security Management Server or Multi Domain Server
**Status:** `200 OK`
