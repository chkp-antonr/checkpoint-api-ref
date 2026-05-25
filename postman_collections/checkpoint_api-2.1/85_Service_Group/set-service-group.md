# set-service-group

**Collection:** Web API (version 2.1) > 85 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-service-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| Ses |   |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Service Group 1",
  "members": {
    "add": "http"
  }
}
```

## Example Responses

### Example 1: set-service-group
**Status:** `200 OK`
