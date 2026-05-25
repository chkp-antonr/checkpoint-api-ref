# clone-group

**Collection:** Web API (version 2.0.1) > 08 Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| Ses |   |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Group 1",
  "members": {
    "add": "New Host 2"
  },
  "groups": "New Group 2"
}
```

## Example Responses

### Example 1: clone-group
**Status:** `200 OK`
