# show-https-rule

**Collection:** Web API (version 2.1) > 126 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Outbound Default Layer",
  "rule-number": 1
}
```

## Example Responses

### Example 1: show-https-rule
**Status:** `200 OK`
