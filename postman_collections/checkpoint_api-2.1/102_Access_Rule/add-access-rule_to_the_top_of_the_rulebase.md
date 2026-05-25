# add-access-rule to the top of the rulebase

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-access-rule`

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
  "position": "top",
  "name": "Top Rule"
}
```

## Example Responses

### Example 1: add-access-rule to the top of the rulebase
**Status:** `200 OK`
