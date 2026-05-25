# Pre Import Verifier

**Collection:** Web API (version 2.0.1) > 131 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/export-management`

## Description

Perform Pre Import Verifications

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "pre-import-verification-only": "true",
  "file-path": "/var/log/exported.tgz"
}
```

## Example Responses

### Example 1: Pre Import Verifier
**Status:** `200 OK`
