# run-app-control-update

```json
{
  "command": "run-app-control-update",
  "description": "Runs Application Control & URL Filtering database update.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/run-app-control-update",
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
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Asynchronous task unique identifier. Use show-task command to check the progress of the task.",
        "type": "string",
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
    "run-app-control-update": {
      "description": "Run Application Control & URL Filtering update",
      "request": "POST {{server}}/run-app-control-update\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"tasks\" : [ {\n    \"uid\" : \"292a7c0f-4b42-4cb3-97ea-186b411e1199\",\n    \"type\" : \"task\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1735822160024,\n        \"iso-8601\" : \"2025-01-02T14:49+0200\"\n      },\n      \"last-modifier\" : \"System\",\n      \"creation-time\" : {\n        \"posix\" : 1735822149328,\n        \"iso-8601\" : \"2025-01-02T14:49+0200\"\n      },\n      \"creator\" : \"WEB_API\"\n    },\n    \"available-actions\" : {\n      \"edit\" : \"true\",\n      \"delete\" : \"true\",\n      \"clone\" : \"false\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"comments\" : \"The applications are up-to-date.\",\n    \"color\" : \"black\",\n    \"icon\" : \"General/globalsNa\",\n    \"task-name\" : \"Application Control & URL Filtering\",\n    \"task-id\" : \"b28b2960-effc-4d46-b7cb-3ce7b0bfda38\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"start-time\" : {\n      \"posix\" : 1735822149311,\n      \"iso-8601\" : \"2025-01-02T14:49+0200\"\n    },\n    \"last-update-time\" : {\n      \"posix\" : 1735822160007,\n      \"iso-8601\" : \"2025-01-02T14:49+0200\"\n    },\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"uid\" : \"c02250e8-6c85-4db7-801e-83bd863232d7\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"color\" : \"black\",\n      \"statusCode\" : \"succeeded\",\n      \"statusDescription\" : \"The applications are up-to-date.\",\n      \"taskNotification\" : \"292a7c0f-4b42-4cb3-97ea-186b411e1199\",\n      \"meta-info\" : {\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1735822160037,\n          \"iso-8601\" : \"2025-01-02T14:49+0200\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1735822149376,\n          \"iso-8601\" : \"2025-01-02T14:49+0200\"\n        },\n        \"creator\" : \"WEB_API\"\n      },\n      \"tags\" : [ ],\n      \"icon\" : \"General/globalsNa\",\n      \"comments\" : \"\",\n      \"display-name\" : \"\"\n    } ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.652896",
    "source_file": "run-app-control-update.html"
  }
}
```