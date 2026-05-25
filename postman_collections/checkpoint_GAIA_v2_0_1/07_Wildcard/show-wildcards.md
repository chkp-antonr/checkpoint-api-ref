# show-wildcards

**Collection:** Web API (version 2.0.1) > 07 Wildcard
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-wildcards`

## Description

Displays all Wildcards

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
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-wildcards
**Status:** `200 OK`
