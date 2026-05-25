# check-threat-ioc-feed with new feed

**Collection:** Web API (version 2.0.1) > 108 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/check-threat-ioc-feed`

## Description

Check New Threat IOC Feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "ioc-feed": {
    "name": "new_feed",
    "feed-url": "https://www.feedsresource.com/resource",
    "feed-type": "md5",
    "fields-delimiter": ",",
    "ignore-lines-that-start-with": "!"
  },
  "targets": "corporate-gateway"
}
```

## Example Responses

### Example 1: check-threat-ioc-feed with new feed
**Status:** `200 OK`
