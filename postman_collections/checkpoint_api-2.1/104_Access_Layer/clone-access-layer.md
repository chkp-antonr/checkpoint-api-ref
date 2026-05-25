# clone-access-layer

**Collection:** Web API (version 2.1) > 104 Access Layer
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-access-layer`

## Description

Clone access layer

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

### Example 1: clone-access-layer
**Status:** `200 OK`
