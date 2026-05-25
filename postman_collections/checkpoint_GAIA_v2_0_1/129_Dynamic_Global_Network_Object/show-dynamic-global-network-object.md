# show-dynamic-global-network-object

**Collection:** Web API (version 2.0.1) > 129 Dynamic Global Network Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-dynamic-global-network-object`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "obj_global"
}
```

## Example Responses

### Example 1: show-dynamic-global-network-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "15c6fd57-bce1-4452-804d-d367c84f6606",
  "name": "obj_global",
  "type": "dynamic-global-network-object",
  "domain": {
    "uid": "1e294ce0-367a-11e3-aa6e-0800200c9a66",
    "name": "Global",
    "domain-type": "global domain"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/globalDynamicObject",
  "groups": []
}
```
