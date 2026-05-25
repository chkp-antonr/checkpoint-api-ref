# show-objects of type tag

**Collection:** Web API (version 2.1) > 183 Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-objects`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "order": [
    {
      "DESC": "name"
    }
  ],
  "type": "tag"
}
```

## Example Responses

### Example 1: show-objects of type tag
**Status:** `200 OK`
