# show-software-packages-per-targets

**Collection:** Web API (version 2.0.1) > 135 Package Deployment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-software-packages-per-targets`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "targets.1": "corporate-gateway",
  "display.installed": "no",
  "display.recommended": "any",
  "display.category": "major"
}
```

## Example Responses

### Example 1: show-software-packages-per-targets
**Status:** `200 OK`
