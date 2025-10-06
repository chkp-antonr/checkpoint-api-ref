# set-policy-settings

```json
{
  "command": "set-policy-settings",
  "description": "Edit Policy settings, the changes will be applied after publish.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-policy-settings",
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
        "name": "last-in-cell",
        "description": "Added object after removing the last object in cell.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "restore to default"
        ]
      },
      {
        "name": "none-object-behavior",
        "description": "'None' object behavior. Rules with object 'None' will never be matched.",
        "type": "string",
        "required": false,
        "valid_values": [
          "warning",
          "error",
          "none"
        ]
      },
      {
        "name": "security-access-defaults",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "destination",
        "description": "Destination default value for new rule creation. Any or None.",
        "type": "string",
        "required": false
      },
      {
        "name": "service",
        "description": "Service and Applications default value for new rule creation. Any or None.",
        "type": "string",
        "required": false
      },
      {
        "name": "source",
        "description": "Source default value for new rule creation. Any or None.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "last-in-cell",
        "description": "Added object after removing the last object in cell.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "restore to default"
        ]
      },
      {
        "name": "none-object-behavior",
        "description": "'None' object behavior. Rules with object 'None' will never be matched.",
        "type": "string",
        "required": false,
        "valid_values": [
          "warning",
          "error",
          "none"
        ]
      },
      {
        "name": "security-access-defaults",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "destination",
        "description": "Destination default value identified by name.",
        "type": "string",
        "required": false
      },
      {
        "name": "service",
        "description": "Service and Applications default value identified by name.",
        "type": "string",
        "required": false
      },
      {
        "name": "source",
        "description": "Source default value identified by name.",
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
    "set-policy-settings": {
      "description": "Set Policy settings",
      "request": "POST {{server}}/set-policy-settings\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"security-access-defaults\" : {\n    \"source\" : \"none\",\n    \"destination\" : \"none\",\n    \"service\" : \"none\"\n  },\n  \"last-in-cell\" : \"none\",\n  \"none-object-behavior\" : \"warning\"\n}",
      "response": "{\n  \"security-access-defaults\" : {\n    \"source\" : \"none\",\n    \"destination\" : \"none\",\n    \"service\" : \"none\"\n  },\n  \"last-in-cell\" : \"none\",\n  \"none-object-behavior\" : \"warning\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:18.767225",
    "source_file": "set-policy-settings.html"
  }
}
```