# show-trusted-ca-settings

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-trusted-ca-settings`

## Description

Show trusted CA settings

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

### Example 1: show-trusted-ca-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "automatic-update": false
}
```
