# set cluster and sync interface

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-interface`

## Description

Modify an existing cluster network interface, set interface as 'cluster + sync' with internal topology defined by routes.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "dae6afba-0b11-49b8-911d-df084cba0bba",
  "cluster-network-type": "cluster + sync",
  "ipv4-address": "4.4.4.111",
  "ipv4-mask-length": 22,
  "topology": "internal",
  "topology-settings": {
    "ip-address-behind-this-interface": "network defined by routing"
  },
  "cluster-members": [
    {
      "uid": "db4f8a63-5a94-46d8-b9e0-a63870bded3d",
      "ipv4-address": "4.4.4.1",
      "ipv4-mask-length": 22
    },
    {
      "uid": "baca571e-8ada-4be9-8966-145388f8e238",
      "ipv4-address": "4.4.4.2",
      "ipv4-mask-length": 22
    }
  ]
}
```

## Example Responses

### Example 1: set cluster and sync interface
**Status:** `200 OK`
