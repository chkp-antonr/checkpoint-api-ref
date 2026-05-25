# set-application-site

**Collection:** Web API (version 2.1) > 86 Application
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-application-site`

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
  "new-name": "New Application Site 2",
  "primary-category": "Instant Chat",
  "description": "My New Application Site",
  "additional-categories": {
    "remove": [
      "Instant Chat",
      "Supports Streaming"
    ]
  },
  "url-list": {
    "add": "www.download.com"
  },
  "urls-defined-as-regular-expression": true,
  "groups": "New Application Site Group 1"
}
```

## Example Responses

### Example 1: set-application-site
**Status:** `200 OK`
