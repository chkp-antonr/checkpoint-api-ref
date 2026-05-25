# set-trusted-client (with domain)

**Collection:** Web API (version 2.0.1) > 146 Trusted Client
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-trusted-client`

## Description

Add a domain to a trusted client.<br>In the example below, add the domain "my domain" to the trusted client "my client".<br>Note – Add domain using the domain name and not an UID.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my client",
  "domains-assignment": {
    "add": "my domain"
  }
}
```

## Example Responses

### Example 1: set-trusted-client (with domain)
**Status:** `200 OK`
