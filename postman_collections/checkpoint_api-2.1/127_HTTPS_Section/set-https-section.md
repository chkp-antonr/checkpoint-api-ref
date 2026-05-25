# set-https-section

**Collection:** Web API (version 2.1) > 127 HTTPS Section
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-https-section`

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
  "name": "New Section 1",
  "new-name": "New Section 2"
}
```

## Example Responses

### Example 1: set-https-section
**Status:** `200 OK`
