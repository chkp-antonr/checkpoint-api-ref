# LSM Run Script

**Collection:** Web API (version 2.1) > 176 Provisioning
**Method:** `POST`
**URL:** `{{server}}/v2.1/lsm-run-script`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "targets": [
    "lsm_gateway"
  ],
  "script": "ls -l /"
}
```

## Example Responses

### Example 1: LSM Run Script
**Status:** `200 OK`
