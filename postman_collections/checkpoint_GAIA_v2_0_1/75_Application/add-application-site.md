# add-application-site

**Collection:** Web API (version 2.0.1) > 75 Application
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-application-site`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site 1",
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
  "urls-defined-as-regular-expression": false
}
```

## Example Responses

### Example 1: add-application-site
**Status:** `200 OK`
