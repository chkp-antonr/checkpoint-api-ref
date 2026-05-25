# show-mobile-access-rulebase

**Collection:** Web API (version 2.0.1) > 89 Mobile Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-mobile-access-rulebase`

## Description

Showing the Mobile Access rulebase

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "offset": 0,
  "limit": 20,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-mobile-access-rulebase
**Status:** `200 OK`
