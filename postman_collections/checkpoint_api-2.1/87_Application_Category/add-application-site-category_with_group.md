# add-application-site-category with group

**Collection:** Web API (version 2.1) > 87 Application Category
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-application-site-category`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Category 2",
  "description": "My Application Site category 2",
  "groups": [
    "New Application Site Group 1"
  ]
}
```

## Example Responses

### Example 1: add-application-site-category with group
**Status:** `200 OK`
