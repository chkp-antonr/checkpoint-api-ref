# add-wildcard with group

**Collection:** Web API (version 2.1) > 07 Wildcard
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-wildcard`

## Description

Adds a new Wildcard with group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Wildcard 2",
  "ipv4-address": "192.168.2.1",
  "ipv4-mask-wildcard": "0.0.128.128",
  "groups": [
    "New Group 1",
    "New Group 2"
  ]
}
```

## Example Responses

### Example 1: add-wildcard with group
**Status:** `200 OK`
