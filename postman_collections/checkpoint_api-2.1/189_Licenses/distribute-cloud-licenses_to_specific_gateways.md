# distribute-cloud-licenses to specific gateways

**Collection:** Web API (version 2.1) > 189 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.1/distribute-cloud-licenses`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "targets": [
    "GWA",
    "GWB"
  ]
}
```

## Example Responses

### Example 1: distribute-cloud-licenses to specific gateways
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-8121-5a35a1e3a31e"
}
```
