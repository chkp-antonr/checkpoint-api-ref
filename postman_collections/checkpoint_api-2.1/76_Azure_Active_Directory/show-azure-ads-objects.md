# show-azure-ads-objects

**Collection:** Web API (version 2.1) > 76 Azure Active Directory
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-azure-ads`

## Description

Show All Microsoft Azure Active Directories.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-azure-ads-objects
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "objects": [
    {
      "uid": "cc7bc29e-054e-47a5-a844-f827e085524c",
      "name": "HadasAAD",
      "type": "azure-ad",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "42925e16-0576-4518-a42a-d58ad10e7cba",
      "name": "my_azureAD",
      "type": "azure-ad",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "7a4b2361-9175-4512-b616-a7c8edae69ac",
      "name": "ShiraAAD",
      "type": "azure-ad",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
