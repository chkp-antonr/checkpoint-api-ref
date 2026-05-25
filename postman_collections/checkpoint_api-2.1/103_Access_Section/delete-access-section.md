# delete-access-section

**Collection:** Web API (version 2.1) > 103 Access Section
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-access-section`

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
  "name": "New Section 2"
}
```

## Example Responses

### Example 1: delete-access-section
**Status:** `200 OK`
