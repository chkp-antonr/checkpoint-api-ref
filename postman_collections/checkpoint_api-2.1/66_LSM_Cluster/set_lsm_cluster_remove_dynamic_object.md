# set lsm cluster remove dynamic object

**Collection:** Web API (version 2.1) > 66 LSM Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-lsm-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "lsm_cluster",
  "dynamic-objects": {
    "remove": {
      "name": "dynamic_object_name"
    }
  }
}
```

## Example Responses

### Example 1: set lsm cluster remove dynamic object
**Status:** `200 OK`
