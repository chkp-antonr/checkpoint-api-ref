# login

```json
{
  "command": "login",
  "description": "Log in to the server with username and password. The server shows your session unique identifier. Enter this session unique identifier in the 'X-chkp-sid' header of each request.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/login",
    "headers": [
      {
        "name": "Content-Type",
        "value": "application/json",
        "description": "Send JSON object to use the API Web Services"
      }
    ],
    "body": [
      {
        "name": "user",
        "description": "Administrator user name.",
        "type": "string",
        "required": true
      },
      {
        "name": "password",
        "description": "Administrator password.",
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
        "name": "domain",
        "description": "Use domain to login to specific domain. Domain can be identified by name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "enter-last-published-session",
        "description": "Login to the last published session. Such login is done with the Read Only permissions.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "new-password",
        "description": "Administrator new password. Can only be used for first login, when the administrator password must be changed.",
        "type": "string",
        "required": false
      },
      {
        "name": "read-only",
        "description": "Login with Read Only permissions. This parameter is not considered in case continue-last-session is true.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "session-comments",
        "description": "Session comments. Can be viewed only using the show-session API.",
        "type": "string",
        "required": false
      },
      {
        "name": "session-description",
        "description": "A description of the session's purpose.",
        "type": "string",
        "required": false
      },
      {
        "name": "session-name",
        "description": "Session unique name.",
        "type": "string",
        "required": false
      },
      {
        "name": "session-timeout",
        "description": "Session expiration timeout in seconds. Default 600 seconds.",
        "type": "integer",
        "required": false
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
    "login": {
      "description": "Login request to receive session token.",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"user\" : \"aa\",\n  \"password\" : \"aaaa\"\n}",
      "response": "{\n  \"sid\" : \"97BVpRfN4j81ogN-V2XqGYmw3DDwIhoSn0og8PiKDiM\",\n  \"url\" : \"https://192.0.2.1:443/web_api\",\n  \"uid\" : \"7a13a360-9b24-40d7-acd3-5b50247be33e\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1430032266851,\n    \"iso-8601\" : \"2015-04-26T10:11+0300\"\n  }\n}"
    },
    "login (domain)": {
      "description": "Login to certain domain",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"user\" : \"aa\",\n  \"password\" : \"aaaa\",\n  \"domain\" : \"Domain Name\"\n}",
      "response": "{\n  \"sid\" : \"3MgL4mBU2NfzuFjl5RxlgtRX6Hc8ZYyIR0FP_3RYHAU\",\n  \"url\" : \"https://192.0.2.1:443/web_api\",\n  \"uid\" : \"7586af28-7375-4e19-a052-cb083d918dd0\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1430032266851,\n    \"iso-8601\" : \"2015-04-26T10:11+0300\"\n  }\n}"
    },
    "login to last published session": {
      "description": "Login to last published session",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"user\" : \"aa\",\n  \"password\" : \"aaaa\",\n  \"enter-last-published-session\" : true\n}",
      "response": "{\n  \"uid\" : \"0bd70128-4e5b-414b-9c98-fa00264507d2\",\n  \"sid\" : \"a0-bI7gXp1IBVMDFIXkrheSDEbQOhqV3_XF2qRaY5ac\",\n  \"url\" : \"https://172.23.78.57:4434/web_api\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1469005943038,\n    \"iso-8601\" : \"2016-07-20T12:12+0300\"\n  },\n  \"api-server-version\" : \"1.1\"\n}"
    },
    "login to last session": {
      "description": "Login to the last session",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"user\" : \"aa\",\n  \"password\" : \"aaaa\",\n  \"continue-last-session\" : true\n}",
      "response": "{\n  \"sid\" : \"tdv_CAG-Lm04wSsMxO43NQhsKipw9MT-l-YFG9Z79AA\",\n  \"url\" : \"https://192.0.2.1:443/web_api\",\n  \"uid\" : \"040cdfe8-e967-407c-af34-2c69884f8e9f\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1430032266851,\n    \"iso-8601\" : \"2015-04-26T10:11+0300\"\n  }\n}"
    },
    "login to system domain": {
      "description": "Login to system domain",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"user\" : \"aa\",\n  \"password\" : \"aaaa\",\n  \"domain\" : \"System Data\"\n}",
      "response": "{\n  \"sid\" : \"FGUjxwAVtaHZewYzap4IveDp1STl50iAdxuR3v6rkRo\",\n  \"url\" : \"https://192.0.2.1:443/web_api\",\n  \"uid\" : \"a50785cc-db67-4149-8d61-eb4bef1c4348\",\n  \"session-timeout\" : 600,\n  \"last-login-was-at\" : {\n    \"posix\" : 1430032266851,\n    \"iso-8601\" : \"2015-04-26T10:11+0300\"\n  }\n}"
    },
    "login with API key": {
      "description": "Login with API key without user and password.",
      "request": "POST {{server}}/login\nContent-Type: application/json\n\n{\n  \"api-key\" : \"FFl8+KF1AJ2Tisac6d0K+w==\"\n}",
      "response": "{\n  \"uid\" : \"1c7d98ea-89f9-43fd-8cd1-db291c2200cd\",\n  \"sid\" : \"HzlgNlKqNOKT6UKuFCSo3xZnFTA44IYTFlEiE2PLtL4\",\n  \"url\" : \"https://172.23.78.79:443/web_api\",\n  \"session-timeout\" : 600,\n  \"api-server-version\" : \"1.5\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.585514",
    "source_file": "login.html"
  }
}
```