# show-objects

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
  "type": "object"
}
```

## Example Responses

### Example 1: show-objects
**Status:** `200 OK`
