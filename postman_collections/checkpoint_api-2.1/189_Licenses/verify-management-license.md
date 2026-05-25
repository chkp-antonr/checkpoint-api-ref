# verify-management-license

**Collection:** Web API (version 2.1) > 189 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.1/verify-management-license`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: verify-management-license
**Status:** `200 OK`

**Body:**
```javascript
{
  "license-status": "Verified Successfully",
  "actual-gateways": "5",
  "licensed-gateways": "10"
}
```
