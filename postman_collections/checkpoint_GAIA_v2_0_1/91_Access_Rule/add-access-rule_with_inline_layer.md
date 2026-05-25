# add-access-rule with inline layer

**Collection:** Web API (version 2.0.1) > 91 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-access-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Network",
  "position": 1,
  "name": "Rule 1",
  "action": "Apply Layer",
  "inline-layer": "Inline"
}
```

## Example Responses

### Example 1: add-access-rule with inline layer
**Status:** `200 OK`
