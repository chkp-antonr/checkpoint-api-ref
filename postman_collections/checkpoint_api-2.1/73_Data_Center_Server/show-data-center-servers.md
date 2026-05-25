# show-data-center-servers

**Collection:** Web API (version 2.1) > 73 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-center-servers`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-data-center-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "d5379ada-c7d7-4678-bf55-0776f33b2326",
      "name": "vCenter 1",
      "type": "data-center-server",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    }
  ]
}
```
