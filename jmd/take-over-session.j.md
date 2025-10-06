# take-over-session

```json
{
  "command": "take-over-session",
  "description": "Take ownership of another session and start working on it.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/take-over-session",
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
        "description": "Session unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "disconnect-active-session",
        "description": "Allows taking over of an active session, currently executed by another administrator.",
        "type": "boolean",
        "required": false,
        "default": "false"
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
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
        "name": "application",
        "description": "The name of the application serving the Management API requests.",
        "type": "string",
        "required": false
      },
      {
        "name": "changes",
        "description": "Number of pending changes.",
        "type": "integer",
        "required": false
      },
      {
        "name": "connected-server",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "aquamarine",
          "black",
          "blue",
          "crete blue",
          "burlywood",
          "cyan",
          "dark green",
          "khaki",
          "orchid",
          "dark orange",
          "dark sea green",
          "pink",
          "turquoise",
          "dark blue",
          "firebrick",
          "brown",
          "forest green",
          "gold",
          "dark gold",
          "gray",
          "dark gray",
          "light green",
          "lemon chiffon",
          "coral",
          "sea green",
          "sky blue",
          "magenta",
          "purple",
          "slate blue",
          "violet red",
          "navy blue",
          "olive",
          "orange",
          "red",
          "sienna",
          "yellow",
          "none"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
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
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aquamarine",
          "black",
          "blue",
          "crete blue",
          "burlywood",
          "cyan",
          "dark green",
          "khaki",
          "orchid",
          "dark orange",
          "dark sea green",
          "pink",
          "turquoise",
          "dark blue",
          "firebrick",
          "brown",
          "forest green",
          "gold",
          "dark gold",
          "gray",
          "dark gray",
          "light green",
          "lemon chiffon",
          "coral",
          "sea green",
          "sky blue",
          "magenta",
          "purple",
          "slate blue",
          "violet red",
          "navy blue",
          "olive",
          "orange",
          "red",
          "sienna",
          "yellow",
          "none"
        ]
      },
      {
        "name": "domain",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
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
        "name": "domain-type",
        "description": "Domain type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
      },
      {
        "name": "icon",
        "description": "Object icon.",
        "type": "string",
        "required": false
      },
      {
        "name": "connection-mode",
        "description": "Session connection mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "read write",
          "read only",
          "read write with global lock",
          "read write with cpmi"
        ]
      },
      {
        "name": "description",
        "description": "Session description.",
        "type": "string",
        "required": false
      },
      {
        "name": "email",
        "description": "Administrator email.",
        "type": "string",
        "required": false
      },
      {
        "name": "expired-session",
        "description": "True if the session is expired.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "in-work",
        "description": "True if the session is in work state.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "IP address from which the session was initiated.",
        "type": "string",
        "required": false
      },
      {
        "name": "last-login-time",
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
        "name": "last-logout-time",
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
        "name": "locks",
        "description": "Number of locked objects.",
        "type": "integer",
        "required": false
      },
      {
        "name": "phone-number",
        "description": "Administrator phone number.",
        "type": "string",
        "required": false
      },
      {
        "name": "publish-time",
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
        "name": "session-timeout",
        "description": "Session expiration timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "state",
        "description": "Session state.",
        "type": "string",
        "required": false,
        "valid_values": [
          "open",
          "pending_approval",
          "published",
          "rejected",
          "discarded"
        ]
      },
      {
        "name": "user-name",
        "description": "The name of the logged in user.",
        "type": "string",
        "required": false
      },
      {
        "name": "workflow-history",
        "description": "Show details per each workflow action.",
        "type": "string",
        "required": false
      },
      {
        "name": "workflow-state",
        "description": "Workflow session state.",
        "type": "string",
        "required": false,
        "valid_values": [
          "open",
          "pending_approval",
          "published",
          "rejected",
          "discarded"
        ]
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
    "take-over-session": {
      "description": "Take over an existing session with UID \"41e821a0-3720-11e3-aa6e-0800200c9fde\".",
      "request": "POST {{server}}/take-over-session\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n  \"disconnect-active-session\" : true\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:29.848120",
    "source_file": "take-over-session.html"
  }
}
```