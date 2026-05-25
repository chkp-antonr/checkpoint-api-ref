# clone-security-zone

**Collection:** Web API (version 2.0.1) > 15 Security Zone
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-security-zone`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "SZone1",
  "new-name": "SZone2"
}
```

## Example Responses

### Example 1: clone-security-zone
**Status:** `200 OK`
