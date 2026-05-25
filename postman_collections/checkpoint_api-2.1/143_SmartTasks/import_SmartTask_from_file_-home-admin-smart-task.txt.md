# import SmartTask from file /home/admin/smart-task.txt

**Collection:** Web API (version 2.1) > 143 SmartTasks
**Method:** `POST`
**URL:** `{{server}}/v2.1/import-smart-task`

## Description

Import a SmartTask from a file /home/admin/smart-task.txt to the Management Server.<br>Note:<br>This example assumes a file contains smart task object as json exists in /home/admin/smart-task.txt

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "file-path": "/home/admin/smart-task.txt"
}
```

## Example Responses

### Example 1: import SmartTask from file /home/admin/smart-task.txt
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
