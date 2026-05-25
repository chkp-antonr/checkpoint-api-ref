# set-global-properties with SCV exceptions

**Collection:** Web API (version 2.1) > 171 Global Properties
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-global-properties`

## Description

Specify hosts that can be accessed using the selected services even if the client is not verified

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "remote-access": {
    "scv": {
      "apply-scv-on-simplified-mode-fw-policies": true,
      "exceptions": {
        "add": {
          "hosts": [
            "host1",
            "host2"
          ],
          "services": "AH"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: set-global-properties with SCV exceptions
**Status:** `200 OK`
