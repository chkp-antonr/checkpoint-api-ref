# show-access-rulebase with hits

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-access-rulebase`

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
  "name": "Network",
  "details-level": "standard",
  "use-object-dictionary": true,
  "show-hits": true,
  "hits-settings": {
    "from-date": "2014-01-01",
    "to-date": "2014-12-31T23:59",
    "target": "corporate-gw"
  }
}
```

## Example Responses

### Example 1: show-access-rulebase with hits
**Status:** `200 OK`
