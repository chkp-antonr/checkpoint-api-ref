# delete-global-assignment

**Collection:** Web API (version 2.1) > 139 Global Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-global-assignment`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "global-domain": "Global2",
  "dependent-domain": "domain1"
}
```

## Example Responses

### Example 1: delete-global-assignment
**Status:** `200 OK`
