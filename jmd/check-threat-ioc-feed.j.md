# check-threat-ioc-feed

```json
{
  "command": "check-threat-ioc-feed",
  "description": "Check if a target can reach or parse a threat IOC feed - can work with an existing feed object or with a new one (by providing all relevant feed parameters.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/check-threat-ioc-feed",
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
        "name": "ioc-feed",
        "description": "",
        "type": "array",
        "required": true,
        "default": "Prevent",
        "valid_values": [
          "Prevent",
          "Detect",
          "AccordingToProfile",
          "Inactive"
        ]
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "feed-url",
        "description": "URL of the feed. URL should be written as http or https.",
        "type": "string",
        "required": false
      },
      {
        "name": "action",
        "description": "The feed indicator's action.",
        "type": "string",
        "required": false,
        "default": "Prevent",
        "valid_values": [
          "Prevent",
          "Detect",
          "AccordingToProfile",
          "Inactive"
        ]
      },
      {
        "name": "certificate-id",
        "description": "Certificate SHA-1 fingerprint to access the feed.",
        "type": "string",
        "required": false
      },
      {
        "name": "confidence",
        "description": "Set in order to configure the confidence of the snort protections in snort format. 1-Low, 5-High.",
        "type": "integer",
        "required": false,
        "default": "1",
        "valid_values": [
          "1-5"
        ]
      },
      {
        "name": "custom-comment",
        "description": "Custom IOC feed - the column number of comment.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "custom-confidence",
        "description": "Custom IOC feed - the column number of confidence.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "custom-header",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "header-name",
        "description": "The name of the HTTP header we wish to add.",
        "type": "string",
        "required": false
      },
      {
        "name": "header-value",
        "description": "The name of the HTTP value we wish to add.",
        "type": "string",
        "required": false
      },
      {
        "name": "header-name",
        "description": "The name of the HTTP header we wish to add.",
        "type": "string",
        "required": false
      },
      {
        "name": "header-value",
        "description": "The name of the HTTP value we wish to add.",
        "type": "string",
        "required": false
      },
      {
        "name": "custom-name",
        "description": "Custom IOC feed - the column number of name.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "custom-severity",
        "description": "Custom IOC feed - the column number of severity.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "custom-type",
        "description": "Custom IOC feed - the column number of type in case a specific type is not chosen.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "custom-value",
        "description": "Custom IOC feed - the column number of value in case a specific type is chosen.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-100"
        ]
      },
      {
        "name": "enabled",
        "description": "Sets whether this indicator feed is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "feed-type",
        "description": "Feed type to be enforced.",
        "type": "string",
        "required": false,
        "valid_values": [
          "any type",
          "domain",
          "ip address",
          "md5",
          "url",
          "ip range",
          "mail subject",
          "mail from",
          "mail to",
          "mail reply to",
          "mail cc",
          "sha1",
          "sha256"
        ]
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "password",
        "description": "password for authenticating with the URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "performance-impact",
        "description": "Set in order to configure the performance impact of the snort protections in snort format. 1-Very Low, 4-High.",
        "type": "integer",
        "required": false,
        "default": "4",
        "valid_values": [
          "1-4"
        ]
      },
      {
        "name": "severity",
        "description": "Set in order to configure the severity of the snort protections in snort format. 1-Low, 4-Critical.",
        "type": "integer",
        "required": false,
        "default": "3",
        "valid_values": [
          "1-4"
        ]
      },
      {
        "name": "use-custom-feed-settings",
        "description": "Set in order to configure a custom indicator feed.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-snort-format",
        "description": "Set in order to configure a snort format indicator feed.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "username",
        "description": "username for authenticating with the URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "fields-delimiter",
        "description": "The delimiter that separates between the columns in the feed.",
        "type": "stringDescription:",
        "required": false
      },
      {
        "name": "ignore-lines-that-start-with",
        "description": "A prefix that will determine which lines to ignore.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-gateway-proxy",
        "description": "Use the gateway's proxy for retrieving the feed.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "targets",
        "description": "On what targets to execute this command. Targets may be identified by their name, or object unique identifier.",
        "type": "string",
        "required": true
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "tasks",
        "description": "Asynchronous task unique identifiers.",
        "type": "array",
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
    "check-threat-ioc-feed with existing feed": {
      "description": "Check Existing Threat IOC Feed",
      "request": "POST {{server}}/check-threat-ioc-feed\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"ioc-feed\" : {\n    \"name\" : \"existing_feed\"\n  },\n  \"targets\" : \"corporate-gateway\"\n}",
      "response": ""
    },
    "check-threat-ioc-feed with overrides": {
      "description": "Check Existing Threat IOC Feed With Overrides",
      "request": "POST {{server}}/check-threat-ioc-feed\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"ioc-feed\" : {\n    \"name\" : \"existing_feed\",\n    \"use-gateway-proxy\" : \"false\",\n    \"feed-type\" : \"md5\"\n  },\n  \"targets\" : \"corporate-gateway\"\n}",
      "response": ""
    },
    "check-threat-ioc-feed with new feed": {
      "description": "Check New Threat IOC Feed",
      "request": "POST {{server}}/check-threat-ioc-feed\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"ioc-feed\" : {\n    \"name\" : \"new_feed\",\n    \"feed-url\" : \"https://www.feedsresource.com/resource\",\n    \"feed-type\" : \"md5\",\n    \"fields-delimiter\" : \",\",\n    \"ignore-lines-that-start-with\" : \"!\"\n  },\n  \"targets\" : \"corporate-gateway\"\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:12.197785",
    "source_file": "check-threat-ioc-feed.html"
  }
}
```