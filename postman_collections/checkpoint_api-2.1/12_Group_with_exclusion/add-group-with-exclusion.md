# add-group-with-exclusion

**Collection:** Web API (version 2.1) > 12 Group with exclusion
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-group-with-exclusion`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Group with exclusion",
  "include": "New Group 1",
  "except": "New Group 2"
}
```

## Example Responses

### Example 1: add-group-with-exclusion
**Status:** `200 OK`
