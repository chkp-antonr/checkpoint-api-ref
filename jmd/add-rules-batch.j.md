# add-rules-batch

```json
{
  "command": "add-rules-batch",
  "description": "Creates new rules in batch. Use this API to achieve optimum performance when adding more than one rule. Note: Add multiple rules to a layer in a specific position, incrementing position by one for each rule. Note: Errors and warnings are ignored when using this API, operation will apply changes while ignoring errors. It is not possible to publish changes that contain validations errors. You must use the \"show-validations\" API to see any validation errors and warnings caused by the batch creation. Supported rules types: access-rule, nat-rule, https-rule and threat-exception.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-rules-batch",
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
        "name": "objects",
        "description": "",
        "type": "array",
        "required": true,
        "valid_values": [
          "top",
          "bottom"
        ]
      },
      {
        "name": "layer",
        "description": "Layer name or uid.",
        "type": "string",
        "required": true
      },
      {
        "name": "type",
        "description": "Type of rules to be created. Only types from above are supported.",
        "type": "string",
        "required": true
      },
      {
        "name": "first-position",
        "description": "First rule position.",
        "type": "integerDescription:",
        "required": true
      },
      {
        "name": "top",
        "description": "Add rule on top of specific section identified by uid or name",
        "type": "string",
        "required": false
      },
      {
        "name": "list",
        "description": "List of rules from the same type to be created on the same layer. Use the \"add\" API reference documentation for a single rule command to find the expected fields for the request. For example: to add access-rules, use the \"add-access-rule\" command found in the API reference documentation (under Access Control & NAT). Note: \"set-if-exists\", \"ignore-errors\", \"ignore-warnings\" and \"details-level\" options are not supported when adding a batch of rules.",
        "type": "array",
        "required": true
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Batch task UID. Use show-task command to check the progress of the task.",
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
    "add rules-batch": {
      "description": "Add two access rules, two nat rules and two https rules",
      "request": "POST {{server}}/add-rules-batch\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"objects\" : [ {\n    \"type\" : \"access-rule\",\n    \"layer\" : \"Network\",\n    \"first-position\" : \"top\",\n    \"list\" : [ {\n      \"name\" : \"access rule 1\",\n      \"action\" : \"accept\"\n    }, {\n      \"name\" : \"access rule 2\",\n      \"action\" : \"accept\"\n    } ]\n  }, {\n    \"type\" : \"nat-rule\",\n    \"layer\" : \"Standard\",\n    \"first-position\" : \"top\",\n    \"list\" : [ {\n      \"name\" : \"nat rule 1\"\n    }, {\n      \"name\" : \"nat rule 2\"\n    } ]\n  }, {\n    \"type\" : \"https-rule\",\n    \"layer\" : \"Default Layer\",\n    \"first-position\" : \"top\",\n    \"list\" : [ {\n      \"name\" : \"https rule 1\"\n    }, {\n      \"name\" : \"https rule 2\"\n    } ]\n  } ]\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"add-rules-batch\",\n    \"task-id\" : \"abcdef01-2345-6789-b3e1-ec3bf46e699a\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"progress-description\" : \"Operation Complete\",\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"status\" : \"Batch operation completed successfully\"\n    } ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:08.579799",
    "source_file": "add-rules-batch.html"
  }
}
```