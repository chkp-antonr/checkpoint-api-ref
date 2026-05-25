# show-service-groups as ranges

**Collection:** Web API (version 2.1) > 85 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-service-groups`

## Description

Shows the first 50 service groups with each service group's matched content displayed as ranges of port numbers, and not as Check Point Objects.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "full",
  "show-as-ranges": "true"
}
```

## Example Responses

### Example 1: show-service-groups as ranges
**Status:** `200 OK`
