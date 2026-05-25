# add-service-citrix-tcp

**Collection:** Web API (version 2.0.1) > 83 Service Citrix TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-citrix-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mycitrixtcp",
  "application": "My Citrix Application"
}
```

## Example Responses

### Example 1: add-service-citrix-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "3464de87-7e4c-4dde-8b67-89cf2f46c32c",
  "name": "mycitrixtcp",
  "type": "service-citrix-tcp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/TCPCitrixService",
  "groups": [],
  "application": "My Citrix Application",
  "port": "1494"
}
```
