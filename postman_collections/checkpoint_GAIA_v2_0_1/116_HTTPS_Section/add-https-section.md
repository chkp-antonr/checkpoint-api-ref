# add-https-section

**Collection:** Web API (version 2.0.1) > 116 HTTPS Section
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-https-section`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Default Layer",
  "position": 1,
  "name": "New Section 1"
}
```

## Example Responses

### Example 1: add-https-section
**Status:** `200 OK`
