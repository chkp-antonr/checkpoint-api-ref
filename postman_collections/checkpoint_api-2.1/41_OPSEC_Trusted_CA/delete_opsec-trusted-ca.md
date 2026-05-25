# delete opsec-trusted-ca

**Collection:** Web API (version 2.1) > 41 OPSEC Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-opsec-trusted-ca`

## Description

Delete opsec trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "opsec_ca"
}
```

## Example Responses

### Example 1: delete opsec-trusted-ca
**Status:** `200 OK`
