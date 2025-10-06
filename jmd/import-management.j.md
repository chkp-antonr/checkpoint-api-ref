# import-management

```json
{
  "command": "import-management",
  "description": "Import the primary Security Management Server database or the primary Multi-Domain Server database or the single Domain database and the applicable Check Point configuration. After the import starts, the session expires and you must login again.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/import-management",
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
        "description": "Path to the exported database file to be imported.",
        "type": "string",
        "required": true
      },
      {
        "name": "domain-name",
        "description": "Domain name to be imported. Must be unique in the Multi-Domain Server.Required only for importing the Security Management Server into the Multi-Domain Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "change-ips",
        "description": "",
        "type": "Object",
        "required": true
      },
      {
        "name": "server-name",
        "description": "The object name of the server that migrates to a new IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "new-ipv4-address",
        "description": "The new IPv4 address of the server that migrates to a new IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "server-name",
        "description": "The object name of the server that migrates to a new IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "new-ipv4-address",
        "description": "The new IPv4 address of the server that migrates to a new IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "domain-ip-address",
        "description": "IPv4 address for the imported Domain.Required only for importing the Security Management Server into the Multi-Domain Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "domain-server-name",
        "description": "Multi-Domain Server name for the imported Domain.Required only for importing the Security Management Server into the Multi-Domain Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "domain-ipv6-address",
        "description": "IPv6 address for the imported Domain.",
        "type": "string",
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
        "description": "Import logs without log indexes.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "include-logs-indexes",
        "description": "Import logs with log indexes.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "keep-cloud-sharing",
        "description": "Preserve the connection of the Management Server to Check Point's Infinity Portal.Use this flag after ensuring that the original Management Server does not communicate with Infinity Portal.Note: resuming the connection is also possible after import with set-cloud-services.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "include-endpoint-configuration",
        "description": "Include import of the Endpoint Security Management configuration files.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "include-endpoint-database",
        "description": "Include import of the Endpoint Security Management database.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "verify-domain-restore",
        "description": "If true, verify that the restore operation is valid for this input file and this environment. Note: Restore operation will not be executed.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "pre-import-verification-only",
        "description": "If true, only runs the pre-import verifications instead of the full import.",
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
      },
      {
        "name": "login-required",
        "description": "If set to \"True\", session is expired and login is required.",
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
    "Import the Security Management Server or Domain Management Server when servers in the environment migrate to new IP addresses": {
      "description": "Import the Security Management Server or Domain Management Server when two servers in the environment migrate to new IP addresses ('MyServer' migrates to 192.0.2.1, and 'MyServer2' migrates to 192.0.2.2)",
      "request": "POST {{server}}/import-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"file-path\" : \"/var/log/exported.tgz\",\n  \"change-ips\" : [ {\n    \"new-ipv4-address\" : \"192.0.2.1\",\n    \"server-name\" : \"MyServer\"\n  }, {\n    \"new-ipv4-address\" : \"192.0.2.2\",\n    \"server-name\" : \"MyServer2\"\n  } ]\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Import domain on the Multi Domain server": {
      "description": "Import domain into Multi Domain Server. The domain name exists within the exported file: /var/log/domain1_exported.tgz",
      "request": "POST {{server}}/import-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"file-path\" : \"/var/log/domain1_exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Import entire Security Management Server or Multi Domain Server": {
      "description": "Import entire Security Management Server or Multi Domain Server",
      "request": "POST {{server}}/import-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"file-path\" : \"/var/log/exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Import Security Management Server as domain in a Multi Domain Server": {
      "description": "Import Security Management Server into Multi Domain Server. domain-name, domain-server-name and domain-ip-address must be given",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"domain-name\" : \"domain1\",\n  \"domain-server-name\" : \"domain1_Server\",\n  \"domain-ip-address\" : \"192.0.2.1\",\n  \"file-path\" : \"/var/log/smc_exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Pre Import Verifier": {
      "description": "Perform Pre Import Verifications",
      "request": "POST {{server}}/export-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"pre-import-verification-only\" : \"true\",\n  \"file-path\" : \"/var/log/exported.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    },
    "Restore domain on the Multi Domain Server": {
      "description": "Restore domain into Multi Domain Server. The domain name exists within the backup file: /var/log/domain1_backup.tgz",
      "request": "POST {{server}}/import-management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"file-path\" : \"/var/log/domain1_backup.tgz\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.446535",
    "source_file": "import-management.html"
  }
}
```