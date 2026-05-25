# ha-full-sync

**Collection:** Web API (version 2.1) > 154 High Availability
**Method:** `POST`
**URL:** `{{server}}/v2.1/ha-full-sync`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mypeer"
}
```

## Example Responses

### Example 1: ha-full-sync
**Status:** `200 OK`
