# show-data-type-file-group

**Collection:** Web API (version 2.0.1) > 53 Data Type File Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-data-type-file-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Archive"
}
```

## Example Responses

### Example 1: show-data-type-file-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "143d58d2-a9dc-4991-836d-c3e716894d92",
  "name": "Archive",
  "type": "data-type-file-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1692228178290,
      "iso-8601": "2023-08-17T02:22+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1692228178290,
      "iso-8601": "2023-08-17T02:22+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "DataLossPrevention/archive_group",
  "file-name": "Archive",
  "visual-string": "Archive files"
}
```
