# add-https-rule with custom fields with lists

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
  "name": "Third Rule",
  "position": 1,
  "source.1": "host1",
  "source.2": "host2",
  "destination.1": "host3",
  "destination.2": "host4",
  "service.1": "https",
  "service.2": "Web_Proxy",
  "action": "Inspect",
  "site-category.1": "alcohol",
  "site-category.2": "education",
  "blade.1": "IPS",
  "blade.2": "Content Awareness",
  "blade.3": "Data Loss Prevention"
}
```

## Example Responses

### Example 1: add-https-rule with custom fields with lists
**Status:** `200 OK`
