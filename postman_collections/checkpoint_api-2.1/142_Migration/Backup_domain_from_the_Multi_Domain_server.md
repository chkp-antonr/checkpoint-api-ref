# Backup domain from the Multi Domain server

**Collection:** Web API (version 2.1) > 142 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.1/export-management`

## Description

Backup domain named domain1 into /var/log/domain1_backup.tgz

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
  "file-path": "/var/log/domain1_backup.tgz",
  "is-domain-backup": true
}
```

## Example Responses

### Example 1: Backup domain from the Multi Domain server
**Status:** `200 OK`
