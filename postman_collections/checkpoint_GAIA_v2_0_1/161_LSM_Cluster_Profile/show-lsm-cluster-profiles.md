# show-lsm-cluster-profiles

**Collection:** Web API (version 2.0.1) > 161 LSM Cluster Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-lsm-cluster-profiles`

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

### Example 1: show-lsm-cluster-profiles
**Status:** `200 OK`
