# Pre Export Verifier

**Collection:** Web API (version 2.1) > 142 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.1/export-management`

## Description

Perform Pre Export Verifications for a target version

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "pre-export-verification-only": "true"
}
```

## Example Responses

### Example 1: Pre Export Verifier
**Status:** `200 OK`
