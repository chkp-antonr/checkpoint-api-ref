# show-repository-package

**Collection:** Web API (version 2.0.1) > 135 Package Deployment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-repository-package`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz"
}
```

## Example Responses

### Example 1: show-repository-package
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "uid": "f30724b9-3e6a-47ba-b3a6-68350c23e49c",
      "type": "task",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1588849130407,
          "iso-8601": "2020-05-07T13:58+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1588849129489,
          "iso-8601": "2020-05-07T13:58+0300"
        },
        "creator": "WEB_API"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "General/globalsNa",
      "task-name": "Getting information for this software package:Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz",
      "task-id": "1f5c667c-d4b8-44fa-b787-4a66d8949a18",
      "status": "succeeded",
      "progress-percentage": 100,
      "start-time": {
        "posix": 1588849129475,
        "iso-8601": "2020-05-07T13:58+0300"
      },
      "last-update-time": {
        "posix": 1588849130398,
        "iso-8601": "2020-05-07T13:58+0300"
      },
      "suppressed": true,
      "task-details": [
        {
          "uid": "6af7b38e-5cec-45ae-ad48-4d211c9dad9b",
          "name": "Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "domainsPreset": null,
          "objectValidationState": null,
          "dynamicContent": null,
          "color": "black",
          "statusCode": null,
          "statusDescription": "",
          "taskNotification": "f30724b9-3e6a-47ba-b3a6-68350c23e49c",
          "size": "792422769",
          "category": "hotfix",
          "releaseDate": "2019-10-27 00:00:00",
          "baseVersion": "R80.20",
          "description": {
            "text": "R80.20 Jumbo Hotfix Accumulator  General availability (Take 118). This package is suitable for Security Gateway and Standalone Gaia 2.6.18 machines only. ",
            "links": []
          },
          "availability": "both",
          "meta-info": {
            "validation-state": "ok",
            "last-modify-time": {
              "posix": 1588849130322,
              "iso-8601": "2020-05-07T13:58+0300"
            },
            "last-modifier": "WEB_API",
            "creation-time": {
              "posix": 1588849130322,
              "iso-8601": "2020-05-07T13:58+0300"
            },
            "creator": "WEB_API"
          },
          "tags": [],
          "icon": "General/globalsNa",
          "comments": "",
          "display-name": "",
          "customFields": null
        }
      ]
    }
  ]
}
```
