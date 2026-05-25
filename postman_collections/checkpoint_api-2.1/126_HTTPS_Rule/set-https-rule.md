# set-https-rule

**Collection:** Web API (version 2.1) > 126 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "rule-number": 1,
  "layer": "Default Layer",
  "new-position": 2
}
```

## Example Responses

### Example 1: set-https-rule
**Status:** `200 OK`
