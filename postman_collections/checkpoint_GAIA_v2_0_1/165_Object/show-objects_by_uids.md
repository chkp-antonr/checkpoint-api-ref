# show-objects by uids

**Collection:** Web API (version 2.0.1) > 165 Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-objects`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uids": [
    "00fa9e3c-b0cd-0f65-e053-08241dc22da2",
    "00fa9e3c-b0cd-0f65-e053-08241dc22da1"
  ]
}
```

## Example Responses

### Example 1: show-objects by uids
**Status:** `200 OK`
