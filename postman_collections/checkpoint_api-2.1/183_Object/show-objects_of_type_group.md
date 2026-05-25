# show-objects of type group

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
      "ASC": "name"
    }
  ],
  "type": "group"
}
```

## Example Responses

### Example 1: show-objects of type group
**Status:** `200 OK`
