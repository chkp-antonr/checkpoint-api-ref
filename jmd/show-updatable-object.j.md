# show-updatable-object

```json
{
  "command": "show-updatable-object",
  "description": "Retrieves an existing Updatable Object from the Management server.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-updatable-object",
    "headers": [
      {
        "name": "Content-Type",
        "value": "application/json",
        "description": "Send JSON object to use the API Web Services"
      },
      {
        "name": "X-chkp-sid",
        "value": "string token",
        "description": "Session unique identifier as it returned by the login request"
      }
    ],
    "body": [
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "name-in-updatable-objects-repository",
        "description": "Object name in the Updatable Objects Repository.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid-in-updatable-objects-repository",
        "description": "Unique identifier of the object in the Updatable Objects Repository.",
        "type": "string",
        "required": false
      },
      {
        "name": "additional-properties",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "description",
        "description": "Description of retrieved Updatable Object.",
        "type": "string",
        "required": false
      },
      {
        "name": "info-text",
        "description": "Information about the Updatable Object IP ranges source.",
        "type": "string",
        "required": false
      },
      {
        "name": "info-url",
        "description": "URL of the Updatable Object IP ranges source.",
        "type": "string",
        "required": false
      },
      {
        "name": "uri",
        "description": "URI of the Updatable Object under the Updatable Objects Repository.",
        "type": "string",
        "required": false
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": false
      },
      {
        "name": "updatable-object-meta-info",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "updated-on-updatable-objects-repository",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "iso-8601",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "posix",
        "description": "N/A",
        "type": "integer",
        "required": false
      }
    ],
    "failure": [
      {
        "name": "message",
        "description": "Operation status.",
        "type": "string",
        "required": false
      },
      {
        "name": "warnings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "errors",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "blocking-errors",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "code",
        "description": "Error code.",
        "type": "string",
        "required": false,
        "valid_values": [
          "generic_error",
          "generic_err_invalid_syntax",
          "generic_err_invalid_parameter_name",
          "not_implemented",
          "generic_internal_error",
          "generic_server_error",
          "generic_server_initializing",
          "generic_err_command_not_found",
          "generic_err_command_version_not_found",
          "generic_err_invalid_api_type",
          "generic_err_invalid_api_object_feature",
          "generic_err_missing_required_parameters",
          "generic_err_missing_required_header",
          "generic_err_invalid_header",
          "generic_err_invalid_parameter",
          "generic_err_normalize",
          "err_bad_url",
          "err_unknown_api_version",
          "err_login_failed_wrong_username_or_password",
          "err_login_failed_more_than_one_opened_session",
          "err_login_failed",
          "err_already_connected",
          "err_normalization_failed",
          "err_validation_failed",
          "err_submit_failed",
          "err_publish_failed",
          "generic_err_missing_session_id",
          "generic_err_wrong_session_id",
          "generic_err_session_expired",
          "generic_err_session_in_use",
          "err_switch_session_failed",
          "err_connect_session_failed",
          "err_assign_session_failed",
          "err_take_over_session_failed",
          "generic_err_no_permissions",
          "err_forbidden",
          "err_not_a_system_domain_session",
          "err_inappropriate_domain_type",
          "generic_err_object_not_found",
          "generic_err_object_field_not_unique",
          "generic_err_object_type_wrong",
          "generic_err_object_locked",
          "generic_err_object_deletion",
          "err_ha_invalid_operation",
          "err_policy_installation_failed",
          "err_policy_verification_failed",
          "err_rulebase_invalid_operation",
          "err_installed_policy_mismatch",
          "err_server_certificate_operation_failed",
          "err_outbound_inspection_certificate_operation_failed",
          "err_gaia_api_login_failed",
          "err_gaia_api_send_command_failed",
          "err_cme_api_send_command_failed",
          "err_cme_api_not_running_failure",
          "err_infinity_unauthorized",
          "err_infinity_network",
          "err_too_many_requests"
        ]
      }
    ],
    "http_codes": {
      "success": [
        200
      ],
      "failure": [
        400,
        401,
        403,
        404,
        409,
        500,
        501
      ]
    }
  },
  "examples": {
    "show-updatable-object": {
      "description": "Show updatable object using it's name",
      "request": "POST {{server}}/show-updatable-object\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"CodeBuild US East 1\"\n}",
      "response": "{\n  \"uid\" : \"1506cdeb-c132-4d28-bca5-95eb07e12828\",\n  \"name\" : \"CodeBuild US East 1\",\n  \"type\" : \"updatable-object\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"name-in-updatable-objects-repository\" : \"CodeBuild US East 1\",\n  \"uid-in-updatable-objects-repository\" : \"65fcda90-774d-3efc-8402-e814cb89aa9c\",\n  \"additional-properties\" : {\n    \"description\" : \"Amazon CodeBuild is a build service that compiles source code, runs tests, and produces software packages.\",\n    \"info-text\" : \"Amazon Web Services IP address ranges info page\",\n    \"info-url\" : \"http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html\",\n    \"uri\" : \"/Updatable Objects/Amazon Web Services/CodeBuild\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1516634291420,\n      \"iso-8601\" : \"2018-01-22T17:18+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1516634291420,\n      \"iso-8601\" : \"2018-01-22T17:18+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"@app/cp_aws_codebuild\",\n  \"updatable-object-meta-info\" : {\n    \"updated-on-updatable-objects-repository\" : {\n      \"posix\" : 1516633264623,\n      \"iso-8601\" : \"2018-01-22T17:01+0200\"\n    }\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:29.178033",
    "source_file": "show-updatable-object.html"
  }
}
```