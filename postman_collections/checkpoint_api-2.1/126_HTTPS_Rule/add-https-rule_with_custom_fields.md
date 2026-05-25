# add-https-rule with custom fields

**Collection:** Web API (version 2.1) > 126 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "layer": "Default Layer",
  "name": "Second Rule",
  "position": 1,
  "source": "host1",
  "destination": "host2",
  "service": "https",
  "action": "Bypass",
  "site-category": "alcohol",
  "blade": "IPS"
}
```

## Example Responses

### Example 1: add-https-rule with custom fields
**Status:** `200 OK`
