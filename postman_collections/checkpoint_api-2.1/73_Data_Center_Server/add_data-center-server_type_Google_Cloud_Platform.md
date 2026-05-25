# add data-center-server type Google Cloud Platform

**Collection:** Web API (version 2.1) > 73 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-center-server`

## Description

Add data center server of type Google Cloud Platform,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_gcp",
  "type": "gcp",
  "authentication-method": "vm-instance-authentication"
}
```

## Example Responses

### Example 1: add data-center-server type Google Cloud Platform
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
