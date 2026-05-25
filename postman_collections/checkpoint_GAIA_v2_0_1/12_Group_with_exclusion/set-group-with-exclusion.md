# set-group-with-exclusion

**Collection:** Web API (version 2.0.1) > 12 Group with exclusion
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-group-with-exclusion`

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
  "include": "New Group 2",
  "except": "New Group 1"
}
```

## Example Responses

### Example 1: set-group-with-exclusion
**Status:** `200 OK`
