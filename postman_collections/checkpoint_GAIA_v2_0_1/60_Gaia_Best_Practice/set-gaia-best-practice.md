# set-gaia-best-practice

**Collection:** Web API (version 2.0.1) > 60 Gaia Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-gaia-best-practice`

## Description

Modify a Gaia Best Practice created by the user (user-defined)

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "af439463-8370-416b-8bab-55e702a37274",
  "description": "This is a new description for the Best Practice.",
  "new-name": "Edited Best Practice"
}
```

## Example Responses

### Example 1: set-gaia-best-practice
**Status:** `200 OK`
