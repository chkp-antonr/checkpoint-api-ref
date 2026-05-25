# add-service-compound-tcp

**Collection:** Web API (version 2.0.1) > 84 Service Compound TCP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-service-compound-tcp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mycompoundtcp",
  "compound-service": "pointcast",
  "keep-connections-open-after-policy-installation": "True"
}
```

## Example Responses

### Example 1: add-service-compound-tcp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1f0f2270-b297-4400-afa4-d9f56a1cb407",
  "name": "mycompoundtcp",
  "type": "service-compound-tcp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Services/CompoundTCPService",
  "groups": [],
  "keep-connections-open-after-policy-installation": true,
  "compound-service": "pointcast",
  "port": "80"
}
```
