# set-threat-layer

**Collection:** Web API (version 2.1) > 120 Threat Layer
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-layer`

## Description

Set threat layer

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
  "new-name": "New Layer 2"
}
```

## Example Responses

### Example 1: set-threat-layer
**Status:** `200 OK`
