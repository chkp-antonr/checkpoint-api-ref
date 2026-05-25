# add-application-site-group

**Collection:** Web API (version 2.1) > 88 Application Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-application-site-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site Group 1",
  "members": [
    "facebook",
    "Social Networking",
    "New Application Site 1",
    "New Application Site Category 1"
  ]
}
```

## Example Responses

### Example 1: add-application-site-group
**Status:** `200 OK`
