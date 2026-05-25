# Import the Security Management Server or Domain Management Server when servers in the environment migrate to new IP addresses

**Collection:** Web API (version 2.1) > 142 Migration
**Method:** `POST`
**URL:** `{{server}}/v2.1/import-management`

## Description

Import the Security Management Server or Domain Management Server when two servers in the environment migrate to new IP addresses ('MyServer' migrates to 192.0.2.1, and 'MyServer2' migrates to 192.0.2.2)

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/var/log/exported.tgz",
  "change-ips": [
    {
      "new-ipv4-address": "192.0.2.1",
      "server-name": "MyServer"
    },
    {
      "new-ipv4-address": "192.0.2.2",
      "server-name": "MyServer2"
    }
  ]
}
```

## Example Responses

### Example 1: Import the Security Management Server or Domain Management Server when servers in the environment migrate to new IP addresses
**Status:** `200 OK`
