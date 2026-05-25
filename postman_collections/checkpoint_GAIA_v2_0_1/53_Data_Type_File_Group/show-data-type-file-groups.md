# show-data-type-file-groups

**Collection:** Web API (version 2.0.1) > 53 Data Type File Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-data-type-file-groups`

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

### Example 1: show-data-type-file-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 14,
  "total": 14,
  "objects": [
    {
      "uid": "143d58d2-a9dc-4991-836d-c3e716894d92",
      "name": "Archive",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/archive_group",
      "color": "black"
    },
    {
      "uid": "2b916acf-319c-468b-be47-d691361d9b63",
      "name": "Database",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/database_group",
      "color": "black"
    },
    {
      "uid": "51e4ba1e-618a-4314-a622-12978e30267b",
      "name": "Drawing",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/drawing_group",
      "color": "black"
    },
    {
      "uid": "b82f7447-4ba1-443c-a58c-3778b46993a4",
      "name": "Email",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/email_group",
      "color": "black"
    },
    {
      "uid": "d1878c9b-2c6f-4764-83d3-64d788c1c1f8",
      "name": "Executable",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/exe_group",
      "color": "black"
    },
    {
      "uid": "2979451d-2610-4d4a-bde2-c766bbd50dcf",
      "name": "Graphic",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/graphics_group",
      "color": "black"
    },
    {
      "uid": "70d5569a-aa9b-4fcf-87a9-179d24f08b44",
      "name": "Image",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/photo_group",
      "color": "black"
    },
    {
      "uid": "921fa8da-5f4e-4d29-baae-cf70e38439a0",
      "name": "Markup",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/html_group",
      "color": "black"
    },
    {
      "uid": "8bda97b4-79e8-42f5-bd88-606c18bb825e",
      "name": "Multimedia",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/multimedia_group",
      "color": "black"
    },
    {
      "uid": "22874c45-db80-440a-942c-78c3045a7c31",
      "name": "Presentation",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/ppt_group",
      "color": "black"
    },
    {
      "uid": "4c0c70ff-7555-467c-8b50-2894388aea1e",
      "name": "Spreadsheet",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/spreadsheet_group",
      "color": "black"
    },
    {
      "uid": "4d1c73fb-2e7e-4108-b3cb-1ac036d6d294",
      "name": "Text",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/text_group",
      "color": "black"
    },
    {
      "uid": "5d14b031-f3a9-431b-82a6-9f5e1bca77e8",
      "name": "Viewer",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/viewer_group",
      "color": "black"
    },
    {
      "uid": "ad38c839-f2eb-4d2b-bd31-6f80ded598bb",
      "name": "Word",
      "type": "data-type-file-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "DataLossPrevention/word_group",
      "color": "black"
    }
  ]
}
```
