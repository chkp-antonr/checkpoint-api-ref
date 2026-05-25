# delete-azure-ad-object

**Collection:** Web API (version 2.0.1) > 65 Azure Active Directory
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-azure-ad`

## Description

Delete Microsoft Azure Active Directory.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_azureAD"
}
```

## Example Responses

### Example 1: delete-azure-ad-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
