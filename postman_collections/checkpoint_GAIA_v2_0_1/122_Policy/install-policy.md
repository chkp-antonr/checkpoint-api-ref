# install-policy

**Collection:** Web API (version 2.0.1) > 122 Policy
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/install-policy`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "policy-package": "standard",
  "access": true,
  "threat-prevention": true,
  "targets": [
    "corporate-gateway"
  ]
}
```

## Example Responses

### Example 1: install-policy
**Status:** `200 OK`
