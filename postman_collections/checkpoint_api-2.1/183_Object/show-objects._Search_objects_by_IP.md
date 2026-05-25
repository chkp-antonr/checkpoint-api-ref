# show-objects. Search objects by IP

**Collection:** Web API (version 2.1) > 183 Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-objects`

## Description

Searches for the objects using both the IP search and the textual search

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "order": [
    {
      "ASC": "name"
    }
  ],
  "type": "object",
  "filter": "192.0.2.1"
}
```

## Example Responses

### Example 1: show-objects. Search objects by IP
**Status:** `200 OK`
