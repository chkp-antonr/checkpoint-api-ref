# add-access-rule to the bottom of a custom section

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
  "position": {
    "bottom": "My Access Section"
  },
  "name": "Last rule in the section"
}
```

## Example Responses

### Example 1: add-access-rule to the bottom of a custom section
**Status:** `200 OK`
