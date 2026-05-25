# set-https-layer

**Collection:** Web API (version 2.0.1) > 117 HTTPS Layer
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-https-layer`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Layer 1",
  "new-name": "New Layer 2",
  "shared": true
}
```

## Example Responses

### Example 1: set-https-layer
**Status:** `200 OK`
