# show-https-rule with hits

**Collection:** Web API (version 2.1) > 126 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Outbound Default Layer",
  "rule-number": 1,
  "show-hits": true,
  "hits-settings": {
    "from-date": "2014-01-01",
    "to-date": "2014-12-31T23:59",
    "target": "corporate-gw"
  }
}
```

## Example Responses

### Example 1: show-https-rule with hits
**Status:** `200 OK`
