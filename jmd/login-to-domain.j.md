# login-to-domain

```json
{
  "command": "login-to-domain",
  "description": "Login from MDS to other domain.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/login-to-domain",
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
        "name": "domain",
        "description": "Domain identified by the name or UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "continue-last-session",
        "description": "When 'continue-last-session' is set to 'True', the new session would continue where the last session was stopped. This option is available when the administrator has only one session that can be continued. If there is more than one session, see 'switch-session' API.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "read-only",
        "description": "Login with Read Only permissions. This parameter is not considered in case continue-last-session is true.",
        "type": "boolean",
        "required": false,
        "default": "false"
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "sid",
        "description": "Session unique identifier. Enter this session unique identifier in the 'X-chkp-sid' header of each request.",
        "type": "string",
        "required": false
      },
      {
        "name": "api-server-version",
        "description": "API Server version.",
        "type": "string",
        "required": false
      },
      {
        "name": "disk-space-message",
        "description": "Information about the available disk space on the management server.",
        "type": "string",
        "required": false
      },
      {
        "name": "last-login-was-at",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "iso-8601",
        "description": "Date and time represented in international ISO 8601 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "posix",
        "description": "Number of milliseconds that have elapsed since 00:00:00, 1 January 1970.",
        "type": "integer",
        "required": false
      },
      {
        "name": "login-message",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "header",
        "description": "Message header.",
        "type": "string",
        "required": false
      },
      {
        "name": "message",
        "description": "Message content.",
        "type": "string",
        "required": false
      },
      {
        "name": "read-only",
        "description": "True if this session is read only.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "session-timeout",
        "description": "Session expiration timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "standby",
        "description": "True if this management server is in the standby mode.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "uid",
        "description": "Session object unique identifier. This identifier may be used in the discard API to discard changes that were made in this session, when administrator is working from another session, or in the 'switch-session' API.",
        "type": "string",
        "required": false
      },
      {
        "name": "url",
        "description": "URL that was used to reach the API server.",
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
    "login to domain": {
      "description": "Login to domain.",
      "request": "POST {{server}}/login-to-domain\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"domain\" : \"dom83\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": "{\n  \"uid\" : \"2c01da51-ffcb-4c0b-8149-9a4ba7b9107b\",\n  \"sid\" : \"y0_9jL0hnU0_fRgxzxHKJ6A7j893Wk2mqVFfG8Rute0\",\n  \"url\" : \"https://172.23.78.76:443/web_api\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1604328982661,\n    \"iso-8601\" : \"2020-11-02T16:56+0200\"\n  },\n  \"api-server-version\" : \"1.7.1\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.572313",
    "source_file": "login-to-domain.html"
  }
}
```