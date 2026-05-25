# run-threat-emulation-file-types-offline-update

**Collection:** Web API (version 2.1) > 124 Threat Emulation
**Method:** `POST`
**URL:** `{{server}}/v2.1/run-threat-emulation-file-types-offline-update`

## Description

Updates Threat Emulation file types offline.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/tmp/FileTypeUpdate.xml"
}
```

## Example Responses

### Example 1: run-threat-emulation-file-types-offline-update
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "Update of file types supported by Threat Emulation completed successfully."
}
```
