# set-application-site-category

**Collection:** Web API (version 2.0.1) > 76 Application Category
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-application-site-category`

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
