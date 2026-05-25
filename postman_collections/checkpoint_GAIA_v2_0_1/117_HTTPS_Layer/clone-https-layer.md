# clone-https-layer

**Collection:** Web API (version 2.0.1) > 117 HTTPS Layer
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-https-layer`

## Description

Clone https layer

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Layer 1",
  "new-name": "Layer 2"
}
```

## Example Responses

### Example 1: clone-https-layer
**Status:** `200 OK`
