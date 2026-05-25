# set-data-center-server type Microsoft Azure

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-data-center-server`

## Description

Set the authentication method of a data center server of type Microsoft Azure.<br>Make sure to provide all the required arguments for the new authentication method,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_azure",
  "authentication-method": "user-authentication",
  "username": "username@company.onmicrosoft.com",
  "password-base64": "YWRtaW4="
}
```

## Example Responses

### Example 1: set-data-center-server type Microsoft Azure
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "Data Center Operation",
      "task-id": "01234567-89ab-cdef-b4ab-a5aefde29b2e",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": []
    }
  ]
}
```
