# show-identity-tags

**Collection:** Web API (version 2.1) > 149 Identity Tag
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-identity-tags`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full"
}
```

## Example Responses

### Example 1: show-identity-tags
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "b33266ab-aacf-4322-86cf-0b16b25519f6",
      "name": "myidentitytag",
      "type": "identity-tag",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "Tags/ExternalTag",
      "external-identifier": "Cisco ISE security group tag"
    }
  ]
}
```
