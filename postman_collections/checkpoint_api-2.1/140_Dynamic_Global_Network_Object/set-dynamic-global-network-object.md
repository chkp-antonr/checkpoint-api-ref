# set-dynamic-global-network-object

**Collection:** Web API (version 2.1) > 140 Dynamic Global Network Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-dynamic-global-network-object`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "obj_global",
  "new-name": "obj_new_name_global"
}
```

## Example Responses

### Example 1: set-dynamic-global-network-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3c1f64e2-6b63-43dd-b1c0-8171c9b63055",
  "name": "obj_new_name_global",
  "type": "dynamic-global-network-object",
  "domain": {
    "uid": "1e294ce0-367a-11e3-aa6e-0800200c9a66",
    "name": "Global",
    "domain-type": "global domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/globalDynamicObject",
  "groups": []
}
```
