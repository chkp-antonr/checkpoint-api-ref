---
title: Management API Versions
source_html: C:\_Labs\Dev\checkpoint-api-ref-py\out\html\api_versions.html
generatedAt: '2025-10-05T18:45:41.379405+00:00'
---

# Management API Versions
### Overview
The API team regularly updates the API in order to deliver new features, bug fixes, and improve performance.
Some of our changes may at times require modifications to existing applications.
This page describes the versions of the API that are available for use in your applications.
### Check Point Release Versions and the Relevant API Versions
Management APIs versions are released at different intervals than the Check Point Main train/Management releases and do not share the same numbering system.
| Management API Version | Check Point Release |
| --- | --- |
| v2.0.1 | [R82 JHF Take 41](https://sc1.checkpoint.com/documents/Jumbo_HFA/R82/Default.htm) |
| v2 | [R82](https://support.checkpoint.com/results/sk/sk181127) |
| v1.9.1 | [R81.20 JHF Take 43](https://sc1.checkpoint.com/documents/Jumbo_HFA/R81.20/Default.htm) |
| v1.9 | [R81.20](https://support.checkpoint.com/results/sk/sk173903) |
| v1.8.1 | [R81.10 JHF Take 79](https://sc1.checkpoint.com/documents/Jumbo_HFA/R81.10/Default.htm) |
| v1.8 | [R81.10](https://support.checkpoint.com/results/sk/sk170416) |
| v1.7.1 | [R81 JHF Take 34](https://sc1.checkpoint.com/documents/Jumbo_HFA/R81/Default.htm) |
| v1.7 | [R81](https://support.checkpoint.com/results/sk/sk166715) |
| v1.6.1 | [R80.40 JHF Take 78](https://sc1.checkpoint.com/documents/Jumbo_HFA/R80.40/Default.htm) |
| v1.6 | [R80.40](https://support.checkpoint.com/results/sk/sk160736) |
| v1.5 | [R80.30](https://support.checkpoint.com/results/sk/sk144293) |
| v1.4 | [R80.20.M2](https://support.checkpoint.com/results/sk/sk123473) |
| v1.3 | [R80.20](https://support.checkpoint.com/results/sk/sk122485) |
| v1.2 | [R80.20.M1](https://support.checkpoint.com/results/sk/sk123473) |
| v1.1 | [R80.10](https://support.checkpoint.com/results/sk/sk111841) |
| v1 | [R80](https://support.checkpoint.com/results/sk/sk108623) |
See the latest Management API version [here](https://sc1.checkpoint.com/documents/latest/APIs/index.html).
### Get Current Version
To determine the version on your Security Management Server, run one of these API commands:
* `login`
* `show api-versions`
**Example 1**
Command:
```
mgmt_cli login user "admin" password "adminPassword" -f json
```
Result:
```
{
"uid" : "c9eb6726-fc6c-4852-a874-fa353a7d229f",
"sid" : "Y2oSMu9Qx3fgdNOWNzKlQkTOR4uiAV1psiMN4ndJgyw",
"url" : "https://127.0.0.1:443/web_api",
"session-timeout" : 600,
"last-login-was-at" : {
"posix" : 1533532613848,
"iso-8601" : "2018-08-06T08:16+0300"
},
"api-server-version" : "2.0.1"
}
```
**Example 2**
Command:
```
mgmt_cli show api-versions -f json
```
Result:
```
{
"current-version" : "2.0.1",
"supported-versions" : [ "1", "1.1", "1.2", "1.3", "1.4", "1.5", "1.6", "1.6.1", "1.7", "1.8", "1.8.1", "1.9", "1.9.1", "2", "2.0.1"]
}
```
### Executing API Commands in a Specific Version
Each command in API can be called with a specific version. We recommend that you use the latest version of API whenever possible but you can also switch to any of the previous versions at any time.
If an explicit version is not specified, the latest version of Management API is used by default.
Below are examples for how to call the same command (`add host`) in a specific version, using each method:
* SmartConsole CLI
```
add host --version 1.1
```
* mgmt\_cli tool
```
mgmt_cli add host --version 1.1
```
* Gaia CLI
```
mgmt add host --version 1.1
```
* Web Services
```
POST https://<management server>:<port>/web_api/v1.1/add-host
```
If you use the mgmt\_cli tool, you can execute the `login` command to a specific version, and save it as a file.
From now on, when you use this file as your session-id, all of the commands that follow will be executed for this version.
**Example**
Login:
```
mgmt_cli login user "admin" password "adminPassword" --version 1.1 --format json > id.txt
```
Content of id.txt file:
```
{
"uid" : "1675e4a3-265b-46d5-88e9-a8d564d63003",
"sid" : "dKV7uZUn9hM2GE7edtA-QtbeuW3RdMxphPr6IjRsL3U",
"url" : "https://127.0.0.1:443/web_api/v1.1",
"session-timeout" : 600,
"last-login-was-at" : {
"posix" : 1530600944133,
"iso-8601" : "2018-07-03T09:55+0300"
},
"api-server-version" : "1.1"
}
```
The next calls which use this session-id will be called for v1.1 (although not explicitly specified):
```
mgmt_cli add host name "New Host 1" ip-address "192.0.2.1" -s id.txt -f json
mgmt_cli add host name "New Host 1" ip-address "192.0.2.1" --session-id dKV7uZUn9hM2GE7edtA-QtbeuW3RdMxphPr6IjRsL3U -f json
```
### Backward compatibility
The API team maintains backward compatibility so you can continue to use existing scripts even after an upgrade.
The API team can add new fields in the responses and optional new fields in the API requests. However, changes to existing field values in the response or in the request are kept to a minimum.
A breaking change means that backward compatibility is not maintained.
Examples of non-breaking changes:
* Adding an optional field to a request message.
* Adding a field to a response message.
Examples of breaking changes:
* Removing a field from a request message.
* Removing a field from a response message.
* Changing an existing parameter name in a request message.
* Changing an existing parameter name in a response message.
* Changing an existing default value in a request message.