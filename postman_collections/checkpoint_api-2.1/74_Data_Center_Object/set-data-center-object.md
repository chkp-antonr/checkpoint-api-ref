# set-data-center-object

**Collection:** Web API (version 2.1) > 74 Data Center Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-center-object`

## Description

Edits existing data center object.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "VM1 mgmt name",
  "ignore-warnings": true
}
```

## Example Responses

### Example 1: set-data-center-object
**Status:** `200 OK`
