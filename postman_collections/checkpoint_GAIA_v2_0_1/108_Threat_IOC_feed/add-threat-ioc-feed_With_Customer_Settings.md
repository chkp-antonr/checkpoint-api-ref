# add-threat-ioc-feed (With Customer Settings)

**Collection:** Web API (version 2.0.1) > 108 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-threat-ioc-feed`

## Description

Adding a threat IOC feed (With Customer Settings)

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
  "enabled": true,
  "use-custom-feed-settings": true,
  "feed-url": "https://www.feedsresource.com/resource",
  "use-gateway-proxy": false,
  "fields-delimiter": ",",
  "ignore-lines-that-start-with": "!",
  "feed-type": "Any type",
  "action": "prevent",
  "custom-name": 1,
  "custom-value": 2,
  "custom-confidence": 3,
  "custom-comment": 4,
  "custom-severity": 5,
  "custom-type": 6,
  "custom-header": [
    {
      "header-name": "header1",
      "header-value": "value1"
    },
    {
      "header-name": "header2",
      "header-value": "value2"
    }
  ]
}
```

## Example Responses

### Example 1: add-threat-ioc-feed (With Customer Settings)
**Status:** `200 OK`
