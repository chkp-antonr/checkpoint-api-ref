# set-global-properties with Identity Awareness

**Collection:** Web API (version 2.0.1) > 154 Global Properties
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-global-properties`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "identity-awareness": {
    "cache-mode": true,
    "cache-mode-duration": 99
  }
}
```

## Example Responses

### Example 1: set-global-properties with Identity Awareness
**Status:** `200 OK`
