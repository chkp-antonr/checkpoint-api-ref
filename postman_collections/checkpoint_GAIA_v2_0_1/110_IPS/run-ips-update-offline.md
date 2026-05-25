# run-ips-update-offline

**Collection:** Web API (version 2.0.1) > 110 IPS
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/run-ips-update`

## Description

Run IPS update offline

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "package-path": "path/to/update.upf"
}
```

## Example Responses

### Example 1: run-ips-update-offline
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "46c0720c-d9f0-4012-b88e-56baa523086d"
}
```
