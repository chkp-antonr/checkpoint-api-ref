# check-threat-ioc-feed with existing feed

**Collection:** Web API (version 2.1) > 119 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/check-threat-ioc-feed`

## Description

Check Existing Threat IOC Feed

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
    "name": "existing_feed"
  },
  "targets": "corporate-gateway"
}
```

## Example Responses

### Example 1: check-threat-ioc-feed with existing feed
**Status:** `200 OK`
