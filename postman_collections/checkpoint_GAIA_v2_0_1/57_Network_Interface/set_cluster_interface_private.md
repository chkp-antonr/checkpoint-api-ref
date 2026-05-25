# set cluster interface private

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-interface`

## Description

Modify an existing cluster network interface, set interface as 'private'.

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
  "cluster-network-type": "private"
}
```

## Example Responses

### Example 1: set cluster interface private
**Status:** `200 OK`
