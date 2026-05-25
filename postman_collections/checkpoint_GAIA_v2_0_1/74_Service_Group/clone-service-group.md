# clone-service-group

**Collection:** Web API (version 2.0.1) > 74 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-service-group`

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

### Example 1: clone-service-group
**Status:** `200 OK`
