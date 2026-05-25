# add-repository-package

**Collection:** Web API (version 2.1) > 146 Package Deployment
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-repository-package`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "source": "local",
  "name": "Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz",
  "path": "/home/admin/"
}
```

## Example Responses

### Example 1: add-repository-package
**Status:** `200 OK`
