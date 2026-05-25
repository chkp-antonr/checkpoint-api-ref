# show-infinity-idps

**Collection:** Web API (version 2.1) > 175 Infinity Identity Providers
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-infinity-idps`

## Description

Show all infinity IDPs.

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

### Example 1: show-infinity-idps
**Status:** `200 OK`
