# set-updatable-object

**Collection:** Web API (version 2.1) > 78 Updatable Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-updatable-object`

## Description

Edit updatable object using it's name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "CodeBuild US East 1",
  "ignore-warnings": true
}
```

## Example Responses

### Example 1: set-updatable-object
**Status:** `200 OK`
