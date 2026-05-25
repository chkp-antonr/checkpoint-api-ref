# Compliance Scan

**Collection:** Web API (version 2.1) > 68 Compliance
**Method:** `POST`
**URL:** `{{server}}/v2.1/compliance-scan`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: Compliance Scan
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-af68-9164c9e57fff"
}
```
