# add-threat-ioc-feed (With Check Point format/STIX Settings)

**Collection:** Web API (version 2.1) > 119 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-threat-ioc-feed`

## Description

Adding a simple threat IOC feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "ioc_feed",
  "feed-url": "https://www.feedsresource.com/resource",
  "action": "prevent"
}
```

## Example Responses

### Example 1: add-threat-ioc-feed (With Check Point format/STIX Settings)
**Status:** `200 OK`
