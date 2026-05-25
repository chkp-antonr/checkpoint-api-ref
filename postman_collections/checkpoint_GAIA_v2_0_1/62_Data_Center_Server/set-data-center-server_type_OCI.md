# set-data-center-server type OCI

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-data-center-server`

## Description

Set any argument for a data center server of type OCI,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_oci",
  "key_region": "us-ashburn-1"
}
```

## Example Responses

### Example 1: set-data-center-server type OCI
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "Data Center Operation",
      "task-id": "01234567-89ab-cdef-83b9-1b4cb69b0b3c",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": []
    }
  ]
}
```
