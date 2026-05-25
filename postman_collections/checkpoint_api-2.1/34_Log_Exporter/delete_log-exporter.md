# delete log-exporter

**Collection:** Web API (version 2.1) > 34 Log Exporter
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-log-exporter`

## Description

Delete existing log exporter.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newLogExporter"
}
```

## Example Responses

### Example 1: delete log-exporter
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
