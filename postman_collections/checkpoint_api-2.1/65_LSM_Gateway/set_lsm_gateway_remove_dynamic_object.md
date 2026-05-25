# set lsm gateway remove dynamic object

**Collection:** Web API (version 2.1) > 65 LSM Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-lsm-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "lsm_gateway",
  "dynamic-objects": {
    "remove": {
      "name": "dynamic_object_name"
    }
  }
}
```

## Example Responses

### Example 1: set lsm gateway remove dynamic object
**Status:** `200 OK`
