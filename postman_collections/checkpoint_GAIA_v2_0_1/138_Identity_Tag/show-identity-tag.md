# show-identity-tag

**Collection:** Web API (version 2.0.1) > 138 Identity Tag
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-identity-tag`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myidentitytag"
}
```

## Example Responses

### Example 1: show-identity-tag
**Status:** `200 OK`

**Body:**
```javascript
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
```
