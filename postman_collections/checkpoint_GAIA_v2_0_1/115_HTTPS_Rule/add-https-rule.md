# add-https-rule

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
  "position": 1,
  "name": "FirstRule"
}
```

## Example Responses

### Example 1: add-https-rule
**Status:** `200 OK`
