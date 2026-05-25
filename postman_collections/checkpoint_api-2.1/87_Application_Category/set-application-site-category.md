# set-application-site-category

**Collection:** Web API (version 2.1) > 87 Application Category
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-application-site-category`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Category 1",
  "new-name": "New Application Site Category 2",
  "description": "My new Application Site category",
  "groups": "New Application Site Group 1"
}
```

## Example Responses

### Example 1: set-application-site-category
**Status:** `200 OK`
