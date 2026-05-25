# add-threat-protections

**Collection:** Web API (version 2.1) > 116 Threat Protection
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-threat-protections`

## Description

Adding threat protections

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "package-path": "/path/to/community.rules",
  "package-format": "snort"
}
```

## Example Responses

### Example 1: add-threat-protections
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "6b2e5c77-0622-4e7f-a9bf-4e1f21899553"
}
```
