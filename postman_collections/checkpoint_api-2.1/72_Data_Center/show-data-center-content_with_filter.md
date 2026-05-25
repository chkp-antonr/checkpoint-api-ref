# show-data-center-content with filter

**Collection:** Web API (version 2.1) > 72 Data Center
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-center-content`

## Description

Returns the results under the URI "/Datacenters/VMs" which also contain the text "VM1 mgmt"

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "data-center-name": "vCenter 1",
  "filter": {
    "text": "VM1 mgmt",
    "uri": "/Datacenters/VMs"
  }
}
```

## Example Responses

### Example 1: show-data-center-content with filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 4,
  "to": 5,
  "total": 95,
  "objects": [
    {
      "name": "My VM1",
      "type-in-data-center": "VirtualMachine",
      "name-in-data-center": "My VM1",
      "uid-in-data-center": "vm-1",
      "additional-properties": [
        {
          "name": "IP",
          "value": "192.168.0.100"
        },
        {
          "name": "Path",
          "value": "/Datacenters/VMs"
        }
      ]
    },
    {
      "name": "My VM2",
      "type-in-data-center": "VirtualMachine",
      "name-in-data-center": "My VM2",
      "uid-in-data-center": "vm-2",
      "additional-properties": [
        {
          "name": "IP",
          "value": "192.168.0.200"
        },
        {
          "name": "Path",
          "value": "/Datacenters/VMs"
        }
      ]
    }
  ]
}
```
