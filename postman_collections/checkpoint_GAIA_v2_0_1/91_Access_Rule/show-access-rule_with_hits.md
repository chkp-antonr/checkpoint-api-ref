# show-access-rule with hits

**Collection:** Web API (version 2.0.1) > 91 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-access-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Rule 1",
  "layer": "Network",
  "show-hits": true,
  "hits-settings": {
    "from-date": "2014-01-01",
    "to-date": "2014-12-31T23:59",
    "target": "corporate-gw"
  }
}
```

## Example Responses

### Example 1: show-access-rule with hits
**Status:** `200 OK`
