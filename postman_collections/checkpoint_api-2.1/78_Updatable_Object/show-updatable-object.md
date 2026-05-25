# show-updatable-object

**Collection:** Web API (version 2.1) > 78 Updatable Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-updatable-object`

## Description

Show updatable object using it's name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "CodeBuild US East 1"
}
```

## Example Responses

### Example 1: show-updatable-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1506cdeb-c132-4d28-bca5-95eb07e12828",
  "name": "CodeBuild US East 1",
  "type": "updatable-object",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "name-in-updatable-objects-repository": "CodeBuild US East 1",
  "uid-in-updatable-objects-repository": "65fcda90-774d-3efc-8402-e814cb89aa9c",
  "additional-properties": {
    "description": "Amazon CodeBuild is a build service that compiles source code, runs tests, and produces software packages.",
    "info-text": "Amazon Web Services IP address ranges info page",
    "info-url": "http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html",
    "uri": "/Updatable Objects/Amazon Web Services/CodeBuild"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1516634291420,
      "iso-8601": "2018-01-22T17:18+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1516634291420,
      "iso-8601": "2018-01-22T17:18+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "@app/cp_aws_codebuild",
  "updatable-object-meta-info": {
    "updated-on-updatable-objects-repository": {
      "posix": 1516633264623,
      "iso-8601": "2018-01-22T17:01+0200"
    }
  }
}
```
