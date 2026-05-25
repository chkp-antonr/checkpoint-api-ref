# set data-center-server type VMware NSX-T

**Collection:** Web API (version 2.1) > 73 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-data-center-server`

## Description

Set any argument for a data center server of type VMware NSX-T,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_nsxt",
  "username": "admin",
  "hostname": "1.1.1.1"
}
```

## Example Responses

### Example 1: set data-center-server type VMware NSX-T
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
