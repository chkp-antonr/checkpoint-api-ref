# export-management

```json
{
  "command": "export-management",
  "description": "Export the primary Security Management Server database or the primary Multi-Domain Server database or the single Domain database and the applicable Check Point configuration.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/export-management",
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
        "name": "file-path",
        "description": "Path in which the exported database file is saved.Required only when not using pre-export-verification-only flag.",
        "type": "string",
        "required": true
      },
      {
        "name": "domain-name",
        "description": "Domain name to be exported.Required only for exporting a Domain from the Multi-Domain Server or backing up Domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "version",
        "description": "Target version.",
        "type": "string",
        "required": false
      },
      {
        "name": "verify-all-servers",
        "description": "Runs the verification process on all Management Servers and Log Servers.For more information see sk182144.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "days-of-logs",
        "description": "Export last days of logs.",
        "type": "integer",
        "required": false,
        "default": "Not set (all logs are exported)"
      },
      {
        "name": "include-logs",
        "description": "Export logs without log indexes.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "include-logs-indexes",
        "description": "Export logs with log indexes.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "include-endpoint-configuration",
        "description": "Include export of the Endpoint Security Management configuration files.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "include-endpoint-database",
        "description": "Include export of the Endpoint Security Management database.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "is-domain-backup",
        "description": "If true, the exported Domain will be suitable for import on the same Multi-Domain Server only.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "is-smc-to-mds",
        "description": "If true, the exported Security Management Server will be suitable for import on the Multi-Domain Server only.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "pre-export-verification-only",
        "description": "If true, only runs the pre-export verifications instead of the full export.",
        "type": "boolean",
        "required": false,
        "default": "false"
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
    "Backup domain from the Multi Domain server": {
      "description": "Backup domain named domain1 into /var/log/domain1_backup.tgz",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"domain-name\" : \"domain1\",\n  \"file-path\" : \"/var/log/domain1_backup.tgz\",\n  \"is-domain-backup\" : true\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Export domain from the Multi Domain server": {
      "description": "Export domain named domain1 into /var/log/domain1_exported.tgz",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"domain-name\" : \"domain1\",\n  \"file-path\" : \"/var/log/domain1_exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Export entire Security Management Server or Multi Domain Server": {
      "description": "Export entire Security Management Server or Multi Domain Server. If version is not specified, export will be taken to current machine's version",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"version\" : \"R81.10\",\n  \"file-path\" : \"/var/log/exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Export Security Management Server to be imported as domain in a Multi Domain Server": {
      "description": "",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"file-path\" : \"/var/log/smc_exported.tgz\",\n  \"is-smc-to-mds\" : true\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Pre Export Verifier": {
      "description": "Perform Pre Export Verifications for a target version",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"pre-export-verification-only\" : \"true\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.365176",
    "source_file": "export-management.html"
  }
}
```