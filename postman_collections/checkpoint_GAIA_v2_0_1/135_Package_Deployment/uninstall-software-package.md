# uninstall-software-package

**Collection:** Web API (version 2.0.1) > 135 Package Deployment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/uninstall-software-package`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Check_Point_R80_40_JHF_MCD_DEMO_019_MAIN_Bundle_T1_VISIBLE_FULL.tgz",
  "targets.1": "corporate-gateway"
}
```

## Example Responses

### Example 1: uninstall-software-package
**Status:** `200 OK`
