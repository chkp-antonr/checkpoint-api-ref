# show-infinity-idp-objects

**Collection:** Web API (version 2.1) > 175 Infinity Identity Providers
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-infinity-idp-objects`

## Description

Show all infinity IDP objects.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full",
  "offset": 0,
  "limit": 50
}
```

## Example Responses

### Example 1: show-infinity-idp-objects
**Status:** `200 OK`
