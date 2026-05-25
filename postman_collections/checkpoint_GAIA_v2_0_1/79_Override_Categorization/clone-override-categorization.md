# clone-override-categorization

**Collection:** Web API (version 2.0.1) > 79 Override Categorization
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-override-categorization`

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
  "url": "newOverride",
  "new-url": "clonedOverride"
}
```

## Example Responses

### Example 1: clone-override-categorization
**Status:** `200 OK`
