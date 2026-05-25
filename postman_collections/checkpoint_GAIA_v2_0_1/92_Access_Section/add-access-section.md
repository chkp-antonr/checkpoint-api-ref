# add-access-section

**Collection:** Web API (version 2.0.1) > 92 Access Section
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-access-section`

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
  "name": "New Section 1"
}
```

## Example Responses

### Example 1: add-access-section
**Status:** `200 OK`
