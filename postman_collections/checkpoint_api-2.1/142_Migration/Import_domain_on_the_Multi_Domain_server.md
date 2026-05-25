# Import domain on the Multi Domain server

**Collection:** Web API (version 2.1) > 142 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.1/import-management`

## Description

Import domain into Multi Domain Server. The domain name exists within the exported file: /var/log/domain1_exported.tgz

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/var/log/domain1_exported.tgz"
}
```

## Example Responses

### Example 1: Import domain on the Multi Domain server
**Status:** `200 OK`
