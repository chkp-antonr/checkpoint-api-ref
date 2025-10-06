# show-threat-profile

```json
{
  "command": "show-threat-profile",
  "description": "Retrieve existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-threat-profile",
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
        "name": "active-protections-performance-impact",
        "description": "Protections with this performance impact only will be activated in the profile.",
        "type": "string",
        "required": false,
        "valid_values": [
          "high",
          "medium",
          "low",
          "very_low"
        ]
      },
      {
        "name": "active-protections-severity",
        "description": "Protections with this severity only will be activated in the profile.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Critical",
          "High",
          "Medium or above",
          "Low or above"
        ]
      },
      {
        "name": "advanced-dns-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "true",
          "false"
        ]
      },
      {
        "name": "dga-detection",
        "description": "Enable/Disable DGA based domains detection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false"
        ]
      },
      {
        "name": "dns-domain-tunneling",
        "description": "Enable/Disable DNS Tunneling based on domains detection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false"
        ]
      },
      {
        "name": "dns-over-https",
        "description": "Enable/Disable parsing of DNS over HTTPS protocol.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false"
        ]
      },
      {
        "name": "nxns-attack-detection",
        "description": "Enable/Disable NXNS attack detection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false"
        ]
      },
      {
        "name": "confidence-level-high",
        "description": "Action for protections with high confidence level.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Ask",
          "Prevent",
          "Detect"
        ]
      },
      {
        "name": "confidence-level-low",
        "description": "Action for protections with low confidence level.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Ask",
          "Prevent",
          "Detect"
        ]
      },
      {
        "name": "confidence-level-medium",
        "description": "Action for protections with medium confidence level.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Ask",
          "Prevent",
          "Detect"
        ]
      },
      {
        "name": "indicator-overrides",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "Inactive",
          "Ask",
          "Prevent",
          "Detect"
        ]
      },
      {
        "name": "action",
        "description": "The indicator's action in this profile.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Ask",
          "Prevent",
          "Detect"
        ]
      },
      {
        "name": "indicator",
        "description": "The indicator whose action is to be overriden.",
        "type": "string",
        "required": false
      },
      {
        "name": "ips-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "very low",
          "low or very low",
          "medium or lower",
          "high or lower"
        ]
      },
      {
        "name": "exclude-protection-with-performance-impact",
        "description": "Whether to exclude protections depending on their level of performance impact.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "exclude-protection-with-performance-impact-mode",
        "description": "Exclude protections with this level of performance impact.",
        "type": "string",
        "required": false,
        "valid_values": [
          "very low",
          "low or very low",
          "medium or lower",
          "high or lower"
        ]
      },
      {
        "name": "exclude-protection-with-severity",
        "description": "Whether to exclude protections depending on their level of severity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "exclude-protection-with-severity-mode",
        "description": "Exclude protections with this level of severity.",
        "type": "string",
        "required": false,
        "valid_values": [
          "low or above",
          "medium or above",
          "high or above",
          "critical"
        ]
      },
      {
        "name": "newly-updated-protections",
        "description": "Activation of newly updated protections.",
        "type": "string",
        "required": false,
        "valid_values": [
          "active",
          "inactive",
          "staging"
        ]
      },
      {
        "name": "malicious-mail-policy-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "allow",
          "block"
        ]
      },
      {
        "name": "add-customized-text-to-email-body",
        "description": "Add customized text to the malicious email body.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "add-email-subject-prefix",
        "description": "Add a prefix to the malicious email subject.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "add-x-header-to-email",
        "description": "Add an X-Header to the malicious email.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "email-action",
        "description": "Block - block the entire malicious emailAllow - pass the malicious email and apply email changes (like: remove attachments and links, add x-header, etc...).",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow",
          "block"
        ]
      },
      {
        "name": "email-body-customized-text",
        "description": "Customized text for the malicious email body. Available predefined fields: $verdicts$ - the malicious/error attachments/links verdict.",
        "type": "string",
        "required": false
      },
      {
        "name": "email-subject-prefix-text",
        "description": "Prefix for the malicious email subject.",
        "type": "string",
        "required": false
      },
      {
        "name": "failed-to-scan-attachments-text",
        "description": "Replace attachments that failed to be scanned with this text. Available predefined fields: $filename$ - the malicious file name. $md5$ - MD5 of the malicious file.",
        "type": "string",
        "required": false
      },
      {
        "name": "malicious-attachments-text",
        "description": "Replace malicious attachments with this text. Available predefined fields: $filename$ - the malicious file name. $md5$ - MD5 of the malicious file.",
        "type": "string",
        "required": false
      },
      {
        "name": "malicious-links-text",
        "description": "Replace malicious links with this text. Available predefined fields: $neutralized_url$ - neutralized malicious link.",
        "type": "string",
        "required": false
      },
      {
        "name": "remove-attachments-and-links",
        "description": "Remove attachments and links from the malicious email.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-copy",
        "description": "Send a copy of the malicious email to the recipient list.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-copy-list",
        "description": "Recipient list to send a copy of the malicious email.",
        "type": "array",
        "required": false
      },
      {
        "name": "overrides",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "default",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "action",
        "description": "Protection action.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "capture-packets",
        "description": "Capture packets.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "track",
        "description": "Tracking method for protection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "alert",
          "mail",
          "snmp trap",
          "user alert 1",
          "user alert 2",
          "user alert 3"
        ]
      },
      {
        "name": "final",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "action",
        "description": "Protection action.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "capture-packets",
        "description": "Capture packets.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "track",
        "description": "Tracking method for protection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "alert",
          "mail",
          "snmp trap",
          "user alert 1",
          "user alert 2",
          "user alert 3"
        ]
      },
      {
        "name": "override",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "action",
        "description": "Protection action.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Inactive",
          "Detect",
          "Prevent",
          "Drop",
          "Accept"
        ]
      },
      {
        "name": "capture-packets",
        "description": "Capture packets.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "track",
        "description": "Tracking method for protection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "alert",
          "mail",
          "snmp trap",
          "user alert 1",
          "user alert 2",
          "user alert 3"
        ]
      },
      {
        "name": "protection",
        "description": "IPS protection name.",
        "type": "string",
        "required": false
      },
      {
        "name": "protection-external-info",
        "description": "Industry reference (CVE).",
        "type": "array",
        "required": false
      },
      {
        "name": "protection-uid",
        "description": "IPS protection unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "scan-malicious-links",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "max-bytes",
        "description": "Scan links in the first bytes of the mail body.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-links",
        "description": "Maximum links to scan in mail body.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "use-indicators",
        "description": "Indicates whether the profile should make use of indicators.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-bot",
        "description": "Is Anti-Bot blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-virus",
        "description": "Is Anti-Virus blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ips",
        "description": "Is IPS blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-emulation",
        "description": "Is Threat Emulation blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-extraction",
        "description": "Is Threat Extraction blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "zero-phishing",
        "description": "Is Zero Phishing blade activated.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "extended-attributes-to-activate",
        "description": "",
        "type": "array",
        "required": false
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
        "name": "values",
        "description": "",
        "type": "array",
        "required": false
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
        "name": "extended-attributes-to-deactivate",
        "description": "",
        "type": "array",
        "required": false
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
        "name": "values",
        "description": "",
        "type": "array",
        "required": false
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
        "name": "use-extended-attributes",
        "description": "Whether to activate/deactivate IPS protections according to the extended attributes.",
        "type": "boolean",
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
    "show-threat-profile": {
      "description": "",
      "request": "POST {{server}}/show-threat-profile\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Recommended_Profile\"\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:28.899362",
    "source_file": "show-threat-profile.html"
  }
}
```