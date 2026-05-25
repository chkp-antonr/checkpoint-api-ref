# check-threat-ioc-feed with overrides

**Collection:** Web API (version 2.0.1) > 108 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/check-threat-ioc-feed`

## Description

Check Existing Threat IOC Feed With Overrides

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
    "name": "existing_feed",
    "use-gateway-proxy": "false",
    "feed-type": "md5"
  },
  "targets": "corporate-gateway"
}
```

## Example Responses

### Example 1: check-threat-ioc-feed with overrides
**Status:** `200 OK`
