# set-log-exporter

```json
{
  "command": "set-log-exporter",
  "description": "Edit existing log exporter using object name or uid.After you configure a Log Exporter, you must run Install Database.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-log-exporter",
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
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "target-server",
        "description": "Target server port to which logs are exported.",
        "type": "string",
        "required": false
      },
      {
        "name": "target-port",
        "description": "Port number of the target server.",
        "type": "integer",
        "required": false
      },
      {
        "name": "protocol",
        "description": "Protocol used to send logs to the target server.",
        "type": "string",
        "required": false,
        "valid_values": [
          "udp",
          "tcp"
        ]
      },
      {
        "name": "enabled",
        "description": "Indicates whether to enable export.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "attachments",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "add-link-to-log-attachment",
        "description": "Indicates whether to add link to log attachment in SmartView.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "add-link-to-log-details",
        "description": "Indicates whether to add link to log details in SmartView.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "add-log-attachment-id",
        "description": "Indicates whether to add log attachment ID.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "data-manipulation",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "syslog",
          "cef",
          "leef",
          "generic",
          "splunk",
          "logrhythm",
          "json"
        ]
      },
      {
        "name": "aggregate-log-updates",
        "description": "Indicates whether to aggregate log updates.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "format",
        "description": "Logs format.",
        "type": "string",
        "required": false,
        "valid_values": [
          "syslog",
          "cef",
          "leef",
          "generic",
          "splunk",
          "logrhythm",
          "json"
        ]
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
        "name": "target-server",
        "description": "Target server port to which logs are exported.",
        "type": "string",
        "required": false
      },
      {
        "name": "target-port",
        "description": "Port number of the target server.",
        "type": "integer",
        "required": false
      },
      {
        "name": "protocol",
        "description": "Protocol used to send logs to the target server.",
        "type": "string",
        "required": false
      },
      {
        "name": "enabled",
        "description": "Indicates whether to enable export.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "attachments",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "add-link-to-log-attachment",
        "description": "Indicates whether to add link to log attachment in SmartView.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "add-link-to-log-details",
        "description": "Indicates whether to add link to log details in SmartView.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "add-log-attachment-id",
        "description": "Indicates whether to add log attachment ID.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "data-manipulation",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "syslog",
          "cef",
          "leef",
          "generic",
          "splunk",
          "logrhythm",
          "json"
        ]
      },
      {
        "name": "aggregate-log-updates",
        "description": "Indicates whether to aggregate log updates.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "format",
        "description": "Logs format.",
        "type": "string",
        "required": false,
        "valid_values": [
          "syslog",
          "cef",
          "leef",
          "generic",
          "splunk",
          "logrhythm",
          "json"
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
    "set log-exporter": {
      "description": "Edit existing log exporter.",
      "request": "POST {{server}}/set-log-exporter\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"newLogExporter\",\n  \"target-port\" : 999,\n  \"data-manipulation\" : {\n    \"format\" : \"json\"\n  }\n}",
      "response": "{\n  \"uid\" : \"824eed1a-e010-4f7f-a9c2-8d5c82119340\",\n  \"name\" : \"newLogExporter\",\n  \"type\" : \"log-exporter\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1734428475976,\n      \"iso-8601\" : \"2024-12-17T11:41+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1734427947814,\n      \"iso-8601\" : \"2024-12-17T11:32+0200\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : { },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/log_exporter\",\n  \"target-server\" : \"1.2.3.4\",\n  \"target-port\" : 999,\n  \"protocol\" : \"tcp\",\n  \"enabled\" : true,\n  \"attachments\" : {\n    \"add-link-to-log-details\" : false,\n    \"add-link-to-log-attachment\" : true,\n    \"add-log-attachment-id\" : false\n  },\n  \"data-manipulation\" : {\n    \"format\" : \"json\",\n    \"aggregate-log-updates\" : \"true\"\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.858627",
    "source_file": "set-log-exporter.html"
  }
}
```