# clone-wildcard

**Collection:** Web API (version 2.0.1) > 07 Wildcard
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-wildcard`

## Description

Clones an existing Wildcard

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Wildcard 1",
  "new-name": "New Wildcard 3",
  "color": "green",
  "ipv6-address": "2001:db8::1111",
  "ipv6-mask-wildcard": "ffff:ffff::f0f0",
  "groups": "New Group 1"
}
```

## Example Responses

### Example 1: clone-wildcard
**Status:** `200 OK`
