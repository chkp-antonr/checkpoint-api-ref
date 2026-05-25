# delete radius-group

**Collection:** Web API (version 2.1) > 33 RADIUS Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-radius-group`

## Description

Delete an existing radius group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "testgroup",
  "ignore-warnings": "true"
}
```

## Example Responses

### Example 1: delete radius-group
**Status:** `200 OK`
