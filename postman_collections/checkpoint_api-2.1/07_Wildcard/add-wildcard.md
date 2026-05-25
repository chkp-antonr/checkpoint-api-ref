# add-wildcard

**Collection:** Web API (version 2.1) > 07 Wildcard
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-wildcard`

## Description

Adds a new Wildcard

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
  "ipv4-address": "192.168.2.1",
  "ipv4-mask-wildcard": "0.0.0.128"
}
```

## Example Responses

### Example 1: add-wildcard
**Status:** `200 OK`
