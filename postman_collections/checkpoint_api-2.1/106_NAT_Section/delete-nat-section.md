# delete-nat-section

**Collection:** Web API (version 2.1) > 106 NAT Section
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-nat-section`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "package": "standard",
  "name": "New Section 1"
}
```

## Example Responses

### Example 1: delete-nat-section
**Status:** `200 OK`
