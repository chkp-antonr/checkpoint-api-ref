# show-threat-protections

**Collection:** Web API (version 2.0.1) > 105 Threat Protection
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-threat-protections`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-threat-protections
**Status:** `200 OK`
