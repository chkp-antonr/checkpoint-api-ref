# set-https-rule with custom fields

**Collection:** Web API (version 2.0.1) > 115 HTTPS Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-https-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "rule-number": 1,
  "layer": "Default Layer",
  "new-name": "New Rule Name",
  "source.1": "host1",
  "source.2": "host2",
  "destination.1": "host3",
  "destination.2": "host4",
  "service.1": "https",
  "service.2": "Web_Proxy",
  "action": "Inspect",
  "site-category.1": "alcohol",
  "site-category.2": "education",
  "blade.1": "IPS"
}
```

## Example Responses

### Example 1: set-https-rule with custom fields
**Status:** `200 OK`
