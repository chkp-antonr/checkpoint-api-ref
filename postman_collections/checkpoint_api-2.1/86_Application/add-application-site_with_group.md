# add-application-site with group

**Collection:** Web API (version 2.1) > 86 Application
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-application-site`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site 2",
  "primary-category": "Social Networking",
  "description": "My Application Site",
  "additional-categories": [
    "Instant Chat",
    "Supports Streaming",
    "New Application Site Category 1"
  ],
  "url-list": [
    "www.cnet.com",
    "www.stackoverflow.com"
  ],
  "urls-defined-as-regular-expression": true,
  "groups": [
    "New Application Site Group 1"
  ]
}
```

## Example Responses

### Example 1: add-application-site with group
**Status:** `200 OK`
