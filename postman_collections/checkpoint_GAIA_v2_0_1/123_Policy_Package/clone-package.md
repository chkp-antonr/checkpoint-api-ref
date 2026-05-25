# clone-package

**Collection:** Web API (version 2.0.1) > 123 Policy Package
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-package`

## Description

Clone package

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "package 1",
  "new-name": "package 2"
}
```

## Example Responses

### Example 1: clone-package
**Status:** `200 OK`
