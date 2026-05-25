# export SmartTask "Validate Session Name Before Publish" to default file

**Collection:** Web API (version 2.1) > 143 SmartTasks
**Method:** `POST`
**URL:** `{{server}}/v2.1/export-smart-task`

## Description

Export a SmartTask "Validate Session Name Before Publish" to file .<br>Note:<br>This example assumes a smart task called "Validate Session Name Before Publish" exists in the Management Server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Validate Session Name Before Publish"
}
```

## Example Responses

### Example 1: export SmartTask "Validate Session Name Before Publish" to default file
**Status:** `200 OK`

**Body:**
```javascript
{
  "file-path": "/var/log/Validate Session Name Before Publish.txt"
}
```
