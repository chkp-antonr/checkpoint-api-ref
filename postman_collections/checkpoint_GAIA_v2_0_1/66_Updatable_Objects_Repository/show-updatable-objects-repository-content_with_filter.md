# show-updatable-objects-repository-content with filter

**Collection:** Web API (version 2.0.1) > 66 Updatable Objects Repository
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-updatable-objects-repository-content`

## Description

Show objects of the Updatable Objects Repository with "Amazon" in their name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "filter": {
    "text": "Amazon"
  }
}
```

## Example Responses

### Example 1: show-updatable-objects-repository-content with filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "objects": [
    {
      "name-in-updatable-objects-repository": "Amazon AP North-East 1 Servers",
      "uid-in-updatable-objects-repository": "aeef181e-72c8-11e7-9248-54a52c295409",
      "additional-properties": {
        "description": "This is an Amazon object, derived from a link listed below, and all its content is subject to Amazon IPs. Amazon CloudFront is a content delivery network (CDN) that delivers content through a worldwide network of data centers.",
        "info-text": "Amazon Web Services IP address ranges info page",
        "info-url": "http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html",
        "uri": "/ Updatable Objects/Amazon Web Services Servers/CloudFront Servers"
      }
    },
    {
      "name-in-updatable-objects-repository": "CodeBuild AP North-East 1 Servers",
      "uid-in-updatable-objects-repository": "d9eeaf01-965f-365d-8400-9e8ebb45a5cb",
      "additional-properties": {
        "description": "This is an Amazon object, derived from a link listed below, and all its content is subject to Amazon IPs. AWS CodeBuild is a build service that compiles source code, runs tests, and produces software packages.",
        "info-text": "Amazon Web Services IP address ranges info page",
        "info-url": "http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html",
        "uri": "/ Updatable Objects/Amazon Web Services Servers/CodeBuild Servers"
      }
    },
    {
      "name-in-updatable-objects-repository": "CodeBuild AP North-East 2 Servers",
      "uid-in-updatable-objects-repository": "455b99e2-383c-3702-9bdd-54dab06bbbdf",
      "additional-properties": {
        "description": "This is an Amazon object, derived from a link listed below, and all its content is subject to Amazon IPs. AWS CodeBuild is a build service that compiles source code, runs tests, and produces software packages.",
        "info-text": "Amazon Web Services IP address ranges info page",
        "info-url": "http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html",
        "uri": "/ Updatable Objects/Amazon Web Services Servers/CodeBuild Servers"
      }
    }
  ]
}
```
