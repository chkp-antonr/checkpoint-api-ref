# set-session

**Collection:** Web API (version 2.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-session`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "description": "Session to work on ticket number CR00323665"
}
```

## Example Responses

### Example 1: set-session
**Status:** `200 OK`
