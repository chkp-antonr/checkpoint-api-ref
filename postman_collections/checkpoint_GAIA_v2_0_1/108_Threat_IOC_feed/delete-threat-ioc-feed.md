# delete-threat-ioc-feed

**Collection:** Web API (version 2.0.1) > 108 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-threat-ioc-feed`

## Description

Deleting a threat IOC feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "ioc_feed"
}
```

## Example Responses

### Example 1: delete-threat-ioc-feed
**Status:** `200 OK`
