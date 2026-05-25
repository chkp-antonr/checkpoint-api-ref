# show-repository-packages

**Collection:** Web API (version 2.1) > 146 Package Deployment
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-repository-packages`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-repository-packages
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "uid": "f6241fa3-1bca-45a9-a700-968bde6c7219",
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
          "posix": 1588785254969,
          "iso-8601": "2020-05-06T20:14+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1588785254029,
          "iso-8601": "2020-05-06T20:14+0300"
        },
        "creator": "WEB_API"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "General/globalsNa",
      "task-name": "Getting information for this software package:all",
      "task-id": "bdfd4078-8344-4468-b41e-dd3bc70e6da9",
      "status": "succeeded",
      "progress-percentage": 100,
      "start-time": {
        "posix": 1588785254018,
        "iso-8601": "2020-05-06T20:14+0300"
      },
      "last-update-time": {
        "posix": 1588785254958,
        "iso-8601": "2020-05-06T20:14+0300"
      },
      "suppressed": true,
      "task-details": [
        {
          "uid": "00189172-c7b3-40c0-ace2-ec14067d63d5",
          "name": null,
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "color": "black",
          "statusDescription": "",
          "taskNotification": "f6241fa3-1bca-45a9-a700-968bde6c7219",
          "meta-info": {
            "validation-state": "ok",
            "last-modify-time": {
              "posix": 1588785254882,
              "iso-8601": "2020-05-06T20:14+0300"
            },
            "last-modifier": "WEB_API",
            "creation-time": {
              "posix": 1588785254882,
              "iso-8601": "2020-05-06T20:14+0300"
            },
            "creator": "WEB_API"
          },
          "tags": [],
          "icon": "General/globalsNa",
          "comments": "",
          "display-name": "",
          "customFields": null,
          "packages": [
            {
              "category": "hotfix",
              "baseVersion": "R80.20",
              "name": "Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz",
              "size": "792422769",
              "releaseDate": "2019-10-27 00:00:00",
              "description": {
                "text": "R80.20 Jumbo Hotfix Accumulator  General availability (Take 118). This package is suitable for Security Gateway and Standalone Gaia 2.6.18 machines only. ",
                "links": []
              },
              "availability": "both"
            },
            {
              "category": "hotfix",
              "baseVersion": "R80.10",
              "name": "Check_Point_R80_10_JUMBO_HF_Bundle_T259_FULL.tgz",
              "size": "864819325",
              "releaseDate": "",
              "description": {},
              "availability": "local"
            }
          ]
        }
      ]
    }
  ]
}
```
