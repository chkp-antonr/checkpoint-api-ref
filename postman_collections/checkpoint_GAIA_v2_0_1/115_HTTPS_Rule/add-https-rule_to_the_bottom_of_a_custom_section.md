# add-https-rule to the bottom of a custom section

**Collection:** Web API (version 2.0.1) > 115 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-https-rule`

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
  "position": {
    "bottom": "My HTTPS Section"
  },
  "name": "Last rule in the section"
}
```

## Example Responses

### Example 1: add-https-rule to the bottom of a custom section
**Status:** `200 OK`
