# Restore domain on the Multi Domain Server

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/import-management`

## Description

Restore domain into Multi Domain Server. The domain name exists within the backup file: /var/log/domain1_backup.tgz

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/var/log/domain1_backup.tgz"
}
```

## Example Responses

### Example 1: Restore domain on the Multi Domain Server
**Status:** `200 OK`
