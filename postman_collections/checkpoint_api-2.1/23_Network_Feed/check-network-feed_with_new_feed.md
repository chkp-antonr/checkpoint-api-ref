# check-network-feed with new feed

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/check-network-feed`

## Description

Check New Network Feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "network-feed": {
    "name": "new_feed",
    "feed-url": "http://www.feedsresource.com",
    "feed-type": "Domain",
    "fields-delimiter": ",",
    "ignore-lines-that-start-with": "!"
  },
  "targets": "corporate-gateway"
}
```

## Example Responses

### Example 1: check-network-feed with new feed
**Status:** `200 OK`
