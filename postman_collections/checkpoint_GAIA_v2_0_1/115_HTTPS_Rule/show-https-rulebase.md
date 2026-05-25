# show-https-rulebase

**Collection:** Web API (version 2.0.1) > 115 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-https-rulebase`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "offset": 0,
  "limit": 20,
  "name": "Default Layer",
  "details-level": "standard",
  "use-object-dictionary": false
}
```

## Example Responses

### Example 1: show-https-rulebase
**Status:** `200 OK`
