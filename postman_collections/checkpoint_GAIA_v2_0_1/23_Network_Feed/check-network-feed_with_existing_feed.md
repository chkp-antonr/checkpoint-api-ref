# check-network-feed with existing feed

**Collection:** Web API (version 2.0.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/check-network-feed`

## Description

Check Existing Network Feed

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
    "name": "existing_feed"
  },
  "targets": "corporate-gateway"
}
```

## Example Responses

### Example 1: check-network-feed with existing feed
**Status:** `200 OK`
