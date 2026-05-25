# delete lsv-profile

**Collection:** Web API (version 2.1) > 21 LSV Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-lsv-profile`

## Description

Delete an existing LSV Profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "existing lsv-profile"
}
```

## Example Responses

### Example 1: delete lsv-profile
**Status:** `200 OK`
