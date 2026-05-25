# add-service-rpc

**Collection:** Web API (version 2.1) > 92 Service RPC
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-rpc`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New_RPC_Service_1",
  "program-number": 5669,
  "keep-connections-open-after-policy-installation": false
}
```

## Example Responses

### Example 1: add-service-rpc
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "Validation failed with 1 error",
  "code": "generic_error",
  "errors": [
    {
      "message": "More than one object named 'New_RPC_Service_1' exists."
    }
  ]
}
```
