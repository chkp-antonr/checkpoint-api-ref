# show-nat-rulebase-with-hits-filter

**Collection:** Web API (version 2.1) > 105 NAT Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-nat-rulebase`

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
  "limit": 50,
  "details-level": "standard",
  "use-object-dictionary": true,
  "package": "standard",
  "filter": "hits:ZERO",
  "hits-settings": {
    "from-date": "2014-01-01",
    "to-date": "2014-12-31T23:59",
    "target": "corporate-gw"
  }
}
```

## Example Responses

### Example 1: show-nat-rulebase-with-hits-filter
**Status:** `200 OK`
