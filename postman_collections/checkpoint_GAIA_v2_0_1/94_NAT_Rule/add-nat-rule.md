# add-nat-rule

**Collection:** Web API (version 2.0.1) > 94 NAT Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-nat-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "package": "standard",
  "position": "top",
  "comments": "comment example1 nat999",
  "enabled": false,
  "install-on": [
    "Policy Targets"
  ],
  "original-source": "Any",
  "original-destination": "All_Internet"
}
```

## Example Responses

### Example 1: add-nat-rule
**Status:** `200 OK`
