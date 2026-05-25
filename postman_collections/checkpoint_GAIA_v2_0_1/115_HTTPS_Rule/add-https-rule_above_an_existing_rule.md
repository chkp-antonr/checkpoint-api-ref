# add-https-rule above an existing rule

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
    "above": "Last rule"
  },
  "name": "One before the last"
}
```

## Example Responses

### Example 1: add-https-rule above an existing rule
**Status:** `200 OK`
