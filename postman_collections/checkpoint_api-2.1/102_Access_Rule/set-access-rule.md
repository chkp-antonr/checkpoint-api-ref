# set-access-rule

**Collection:** Web API (version 2.1) > 102 Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-access-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Rule 1",
  "layer": "Network",
  "action": "Ask",
  "action-settings": {
    "enable-identity-captive-portal": true,
    "limit": "Upload_1Gbps"
  }
}
```

## Example Responses

### Example 1: set-access-rule
**Status:** `200 OK`
