# add-access-rule with custom fields

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
  "position": 1,
  "name": "Rule 1",
  "custom-fields": {
    "field-1": "first field",
    "field-2": "second field",
    "field-3": "third field"
  }
}
```

## Example Responses

### Example 1: add-access-rule with custom fields
**Status:** `200 OK`
