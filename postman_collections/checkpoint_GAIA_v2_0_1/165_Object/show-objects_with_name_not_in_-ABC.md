# show-objects with name not in ["ABC"]

**Collection:** Web API (version 2.0.1) > 165 Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-objects`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 10,
  "offset": 0,
  "order": [
    {
      "ASC": "name"
    },
    {
      "DESC": "objId"
    }
  ],
  "not": {
    "in": [
      "name",
      "ABC"
    ]
  },
  "type": "object"
}
```

## Example Responses

### Example 1: show-objects with name not in ["ABC"]
**Status:** `200 OK`
