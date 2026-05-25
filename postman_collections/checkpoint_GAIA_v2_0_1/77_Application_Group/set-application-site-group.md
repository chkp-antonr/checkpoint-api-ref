# set-application-site-group

**Collection:** Web API (version 2.0.1) > 77 Application Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-application-site-group`

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
  "name": "New Application Site Group 1",
  "members": {
    "add": "AliveProxy"
  },
  "groups": "New Application Site Group 2"
}
```

## Example Responses

### Example 1: set-application-site-group
**Status:** `200 OK`
