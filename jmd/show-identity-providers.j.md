# show-identity-providers

```json
{
  "command": "show-identity-providers",
  "description": "Retrieve all SAML Identity Providers.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-identity-providers",
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
        "name": "filter",
        "description": "Search expression to filter objects by. The provided text should be exactly the same as it would be given in SmartConsole Object Explorer. The logical operators in the expression ('AND', 'OR') should be provided in capital letters. The search involves both a IP search and a textual search in name, comment, tags etc.",
        "type": "string",
        "required": false
      },
      {
        "name": "limit",
        "description": "The maximal number of returned results.",
        "type": "integer",
        "required": false,
        "default": "50"
      },
      {
        "name": "offset",
        "description": "Number of the results to initially skip.",
        "type": "integer",
        "required": false,
        "default": "0"
      },
      {
        "name": "order",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "name"
        ]
      },
      {
        "name": "ASC",
        "description": "Sorts results by the given field in ascending order.",
        "type": "string",
        "required": false,
        "valid_values": [
          "name"
        ]
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "from",
        "description": "From which element number the query was done.",
        "type": "integer",
        "required": false
      },
      {
        "name": "objects",
        "description": "",
        "type": "array",
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
        "name": "to",
        "description": "To which element number the query was done.",
        "type": "integer",
        "required": false
      },
      {
        "name": "total",
        "description": "Total number of elements returned by the query.",
        "type": "integer",
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
    "show identity-providers": {
      "description": "Shows identity providers.",
      "request": "POST {{server}}/show-identity-providers\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"limit\" : 5,\n  \"offset\" : 0,\n  \"details-level\" : \"full\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 2,\n  \"total\" : 2,\n  \"objects\" : [ {\n    \"uid\" : \"5d1dc574-dfd9-496e-af36-350196a9d62d\",\n    \"name\" : \"TestIdp\",\n    \"type\" : \"identity-provider\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1740375931816,\n        \"iso-8601\" : \"2025-02-24T07:45+0200\"\n      },\n      \"last-modifier\" : \"WEB_API\",\n      \"creation-time\" : {\n        \"posix\" : 1740375186712,\n        \"iso-8601\" : \"2025-02-24T07:33+0200\"\n      },\n      \"creator\" : \"WEB_API\"\n    },\n    \"available-actions\" : {\n      \"edit\" : \"true\",\n      \"delete\" : \"true\",\n      \"clone\" : \"true\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"Objects/AuthenticationServer\",\n    \"usage\" : \"gateway_policy_and_logs\",\n    \"gateway\" : {\n      \"uid\" : \"2f9be5f8-3dfa-4379-87a8-77ff5191c728\",\n      \"name\" : \"TestGW\",\n      \"type\" : \"simple-gateway\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"platform\" : \"open server\",\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1740375122642,\n          \"iso-8601\" : \"2025-02-24T07:32+0200\"\n        },\n        \"last-modifier\" : \"WEB_API\",\n        \"creation-time\" : {\n          \"posix\" : 1740375122642,\n          \"iso-8601\" : \"2025-02-24T07:32+0200\"\n        },\n        \"creator\" : \"WEB_API\"\n      },\n      \"available-actions\" : {\n        \"edit\" : \"true\",\n        \"delete\" : \"true\",\n        \"clone\" : \"not_supported\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : false,\n      \"comments\" : \"\",\n      \"color\" : \"black\",\n      \"icon\" : \"NetworkObjects/gateway\",\n      \"groups\" : [ ],\n      \"nat-settings\" : {\n        \"auto-rule\" : false\n      },\n      \"ipv4-address\" : \"1.1.1.1\",\n      \"dynamic-ip\" : false,\n      \"version\" : \"R82.10\",\n      \"os-name\" : \"Gaia\",\n      \"hardware\" : \"Open server\",\n      \"interfaces\" : [ ],\n      \"network-policy-management\" : false,\n      \"log-server\" : false,\n      \"firewall\" : true,\n      \"firewall-settings\" : {\n        \"auto-maximum-limit-for-concurrent-connections\" : true,\n        \"maximum-limit-for-concurrent-connections\" : 25000,\n        \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n        \"connections-hash-size\" : 131072,\n        \"memory-pool-size\" : 6,\n        \"maximum-memory-pool-size\" : 30\n      },\n      \"vpn\" : false,\n      \"policy-server\" : false,\n      \"mobile-access\" : false,\n      \"application-control\" : false,\n      \"url-filtering\" : false,\n      \"legacy-url-filtering\" : false,\n      \"application-control-and-url-filtering-settings\" : {\n        \"global-settings-mode\" : \"use_global_settings\"\n      },\n      \"content-awareness\" : false,\n      \"monitoring\" : false,\n      \"rtm-traffic-report-per-connection\" : false,\n      \"rtm-traffic-report\" : false,\n      \"rtm-counters-report\" : true,\n      \"anti-spam-and-email-security\" : false,\n      \"threat-prevention-mode\" : \"custom\",\n      \"ips\" : false,\n      \"anti-bot\" : false,\n      \"anti-virus\" : false,\n      \"threat-emulation\" : false,\n      \"threat-extraction\" : false,\n      \"zero-phishing\" : false,\n      \"ips-update-policy\" : \"gateway automatic update\",\n      \"identity-awareness\" : true,\n      \"data-loss-prevention\" : false,\n      \"qos\" : false,\n      \"externally-managed\" : false,\n      \"hit-count\" : true,\n      \"sic-name\" : \"\",\n      \"sic-state\" : \"uninitialized\",\n      \"save-logs-locally\" : false,\n      \"send-alerts-to-server\" : [ \"mgmt_172.23.48.144mgmt_vs_8210_api_main_take_37MGMTdorbe\" ],\n      \"send-logs-to-server\" : [ \"mgmt_172.23.48.144mgmt_vs_8210_api_main_take_37MGMTdorbe\" ],\n      \"send-logs-to-backup-server\" : [ ],\n      \"logs-settings\" : {\n        \"rotate-log-by-file-size\" : false,\n        \"rotate-log-file-size-threshold\" : 1000,\n        \"rotate-log-on-schedule\" : false,\n        \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n        \"alert-when-free-disk-space-below\" : true,\n        \"alert-when-free-disk-space-below-threshold\" : 3000,\n        \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n        \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n        \"delete-when-free-disk-space-below\" : true,\n        \"delete-when-free-disk-space-below-threshold\" : 5000,\n        \"before-delete-keep-logs-from-the-last-days\" : false,\n        \"before-delete-keep-logs-from-the-last-days-threshold\" : 3664,\n        \"before-delete-run-script\" : false,\n        \"before-delete-run-script-command\" : \"\",\n        \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n        \"stop-logging-when-free-disk-space-below\" : true,\n        \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n        \"reject-connections-when-free-disk-space-below-threshold\" : false,\n        \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n        \"reserve-for-packet-capture-threshold\" : 500,\n        \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n        \"delete-index-files-when-index-size-above\" : false,\n        \"delete-index-files-when-index-size-above-threshold\" : 100000,\n        \"delete-index-files-older-than-days\" : false,\n        \"delete-index-files-older-than-days-threshold\" : 14,\n        \"forward-logs-to-log-server\" : false,\n        \"perform-log-rotate-before-log-forwarding\" : false,\n        \"update-account-log-every\" : 3600,\n        \"detect-new-citrix-ica-application-names\" : false,\n        \"turn-on-qos-logging\" : true,\n        \"distribute-logs-between-all-active-servers\" : false\n      },\n      \"platform-portal-settings\" : {\n        \"enabled\" : true,\n        \"portal-web-settings\" : {\n          \"main-url\" : \"https://1.1.1.1/\",\n          \"ip-address\" : \"1.1.1.1\",\n          \"aliases\" : [ ]\n        },\n        \"accessibility\" : {\n          \"allow-access-from\" : \"RULE_BASE\"\n        }\n      },\n      \"nat-hide-internal-interfaces\" : false,\n      \"communication-with-servers-behind-nat\" : {\n        \"override-profile\" : false\n      },\n      \"fetch-policy\" : [ \"mgmt_172.23.48.144mgmt_vs_8210_api_main_take_37MGMTdorbe\" ],\n      \"advanced-settings\" : {\n        \"sam\" : {\n          \"forward-to-other-sam-servers\" : false,\n          \"purge-sam-file\" : {\n            \"enabled\" : false,\n            \"purge-when-size-reaches-to\" : 100\n          },\n          \"use-early-versions\" : {\n            \"enabled\" : false\n          }\n        },\n        \"connection-persistence\" : \"rematch-connections\"\n      },\n      \"enable-https-inspection\" : false,\n      \"https-inspection\" : {\n        \"bypass-on-failure\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : true\n        },\n        \"site-categorization-allow-mode\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : \"hold\"\n        },\n        \"deny-untrusted-server-cert\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : false\n        },\n        \"deny-expired-server-cert\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : false\n        },\n        \"outbound-certificate\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : \"\"\n        },\n        \"bypass-on-client-failure\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : true\n        },\n        \"bypass-under-load\" : {\n          \"value\" : false\n        },\n        \"deployment-mode\" : \"full\",\n        \"deny-revoked-server-cert\" : {\n          \"override-profile\" : false,\n          \"profile-value\" : true\n        }\n      },\n      \"zero-phishing-settings\" : {\n        \"gateway-fqdn-mode\" : \"automatic\"\n      },\n      \"auto-topology-use-custom-recalculation-time\" : false,\n      \"auto-topology-custom-recalculation-time\" : 10,\n      \"identity-awareness-settings\" : {\n        \"remote-access\" : false,\n        \"browser-based-authentication\" : true,\n        \"identity-agent\" : true,\n        \"identity-collector\" : false,\n        \"ad-query\" : false,\n        \"terminal-servers\" : false,\n        \"radius-accounting\" : false,\n        \"collecting-identities\" : false,\n        \"identity-agent-settings\" : {\n          \"agents-interval-keepalive\" : 5,\n          \"user-reauthenticate-interval\" : 480,\n          \"identity-agent-portal-settings\" : {\n            \"portal-web-settings\" : {\n              \"main-url\" : \"https://0.0.0.0/_IAAgent\",\n              \"ip-address\" : \"0.0.0.0\",\n              \"aliases\" : [ ]\n            },\n            \"accessibility\" : {\n              \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n              \"internal-access-settings\" : {\n                \"undefined\" : false,\n                \"dmz\" : false,\n                \"vpn\" : false\n              }\n            }\n          },\n          \"authentication-settings\" : {\n            \"authentication-method\" : \"defined_on_user\",\n            \"users-directories\" : {\n              \"internal-users\" : false,\n              \"external-user-profile\" : false,\n              \"users-from-external-directories\" : \"none\",\n              \"specific\" : [ ]\n            }\n          }\n        },\n        \"browser-based-authentication-settings\" : {\n          \"browser-based-authentication-portal-settings\" : {\n            \"portal-web-settings\" : {\n              \"main-url\" : \"https://1.1.1.1/connect\",\n              \"ip-address\" : \"1.1.1.1\",\n              \"aliases\" : [ ]\n            },\n            \"accessibility\" : {\n              \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n              \"internal-access-settings\" : {\n                \"undefined\" : false,\n                \"dmz\" : false,\n                \"vpn\" : false\n              }\n            }\n          },\n          \"authentication-settings\" : {\n            \"authentication-method\" : \"defined_on_user\",\n            \"users-directories\" : {\n              \"internal-users\" : false,\n              \"external-user-profile\" : false,\n              \"users-from-external-directories\" : \"none\",\n              \"specific\" : [ ]\n            },\n            \"identity-provider\" : [ ]\n          }\n        },\n        \"proxy-settings\" : {\n          \"detect-using-x-forward-for\" : false\n        },\n        \"identity-based-enforcement\" : \"on\",\n        \"identity-web-api\" : false\n      },\n      \"proxy-settings\" : {\n        \"use-custom-proxy\" : false\n      }\n    },\n    \"service\" : \"identity awareness\",\n    \"required-identifier\" : \"https://1.1.1.1/connect/spPortal/ACS/ID/0e4cae10-43f9-4b66-87a8-931d5285df11\",\n    \"reply-urls\" : [ \"https://1.1.1.1/connect/spPortal/ACS/Login/0e4cae10-43f9-4b66-87a8-931d5285df11\" ],\n    \"data-receiving\" : \"manually\",\n    \"base64-metadata-file\" : \"PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48RW50aXR5RGVzY3JpcHRvciBJRD0iXzkwMzU3YWM3LWQ4N2ItNDczZi05Njg2LTEzZjEyOTcwYWJhYiIgZW50aXR5SUQ9Imh0dHBzOi8vc3RzLndpbmRvd3MubmV0LzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy8iIHhtbG5zPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6bWV0YWRhdGEiPjxTaWduYXR1cmUgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjxTaWduZWRJbmZvPjxDYW5vbmljYWxpemF0aW9uTWV0aG9kIEFsZ29yaXRobT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8xMC94bWwtZXhjLWMxNG4jIiAvPjxTaWduYXR1cmVNZXRob2QgQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNyc2Etc2hhMjU2IiAvPjxSZWZlcmVuY2UgVVJJPSIjXzkwMzU3YWM3LWQ4N2ItNDczZi05Njg2LTEzZjEyOTcwYWJhYiI+PFRyYW5zZm9ybXM+PFRyYW5zZm9ybSBBbGdvcml0aG09Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyNlbnZlbG9wZWQtc2lnbmF0dXJlIiAvPjxUcmFuc2Zvcm0gQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzEwL3htbC1leGMtYzE0biMiIC8+PC9UcmFuc2Zvcm1zPjxEaWdlc3RNZXRob2QgQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyNzaGEyNTYiIC8+PERpZ2VzdFZhbHVlPnBPazZnV2QyakNCTzlIb2k4dlp3c3Nqc0VEdE0vYzhKN0E3QmRCUGsvMGc9PC9EaWdlc3RWYWx1ZT48L1JlZmVyZW5jZT48L1NpZ25lZEluZm8+PFNpZ25hdHVyZVZhbHVlPnJIMXVnV0tkbUpCR0c0ckJJcUVFbUhGeEpMVHBRZGp1eUJKV01DTEtMaDNxL250Qksyd2JRQ1dSV0d2MjM0K2xRMWtXNVdjdDFmQlNUcDI1VDU2dis2V21GZnZad3dQb3p4U3F6cURrTzdhclA0Qm50MEh6a0QvRm1MQVZEdE83d3RRVzlsK3R2QkhMT241VkVDTzJ6RVU0anBSTXNnWDFkMUZIckk2M3o4dDZLcm13Q3ljN0hVTGk3WXlaREc0ckt1aUFIU2ZuNWpkRExLV2VVQnh4YWZtd2V1Q1BzVGpEbGcrNnQrYVFqNDl2cjR3N0htcmtCZmNTaXU0VCtYbnBLSG9KaW5TU2YrWFJ1eW1razBiQnJXdVlnQit1YWZmMmEydXV4RFB1ZEtHUXFoRSs5MnUrZnpJbWp0ZjRpM3pNYThOSGVRdDg5ZXBITVluYTNaemE1dz09PC9TaWduYXR1cmVWYWx1ZT48S2V5SW5mbz48WDUwOURhdGE+PFg1MDlDZXJ0aWZpY2F0ZT5NSUlDOERDQ0FkaWdBd0lCQWdJUVEwVmVaS3VQS29KUFFoWjRoQ2lkc0RBTkJna3Foa2lHOXcwQkFRc0ZBREEwTVRJd01BWURWUVFERXlsTmFXTnliM052Wm5RZ1FYcDFjbVVnUm1Wa1pYSmhkR1ZrSUZOVFR5QkRaWEowYVdacFkyRjBaVEFlRncweE9EQTBNVFV4TVRJek16TmFGdzB5TVRBME1UVXhNVEl6TXpOYU1EUXhNakF3QmdOVkJBTVRLVTFwWTNKdmMyOW1kQ0JCZW5WeVpTQkdaV1JsY21GMFpXUWdVMU5QSUVObGNuUnBabWxqWVhSbE1JSUJJakFOQmdrcWhraUc5dzBCQVFFRkFBT0NBUThBTUlJQkNnS0NBUUVBNFV1amFHdDhYWjg5dnV2eWt5UVc1WG9uLzhSL2lQdHo0YWIwTTN0TVV2R1h6M1V4dFdaU0UrVEdYcnYzd1R0SzArOEZrTXl1SmFIRklwSy80VURGaUZNckJsc0dGdXZrU3NaeVYyM2ZTRjd6Wml5VFk2VDdBMHArZ3M1MDVYRDlHQWI5VmJkd0dHMCtLQ1Z5aXNWUWdWMkl3SmdpeWhxd0VDb2N3QnJhbjdudUsrVEVORDJsMmY5WXJ4NW9STUVOejcwd2x5SDM2T1pCbXQwazU5OC9XaDBIRFlMWmVvMGR5U1dyTnd3ZVl2U3hFOC9NZG00M1hFdVN6YmpUemZzTTB2VVJ3RkJTclVMRWFETzEvSVAyVXI3QnNnSHdSSS94Zm9xSW1LMUtrcFVxMEFsY1RBaTN2MXU5ekMvcUxnUHdBeVFJdnc5VUNzaXJyUEEwWTBZT2hRSURBUUFCTUEwR0NTcUdTSWIzRFFFQkN3VUFBNElCQVFEY2pvamRHei9BSUNqak0wWjdtWWxnUDV6YnNhUTVkQzJjamY0REpxbWttc1d1ZlJwQzRzYnN1aDg3MGNDQktjdXZoK29HaXpCUUhyUG00VGhJdmZJbEtMOFhqTEFYYkZ1UlBvSEFnMDhzTFhkdlBUQlROdkRGMU1ob3FOczJqNmVGcS9kTnVxdmVCSHI1RDV0S25WMlhCR0VIRTlSRTlXVGtaUU9jMGhIbUN3TW1jWW9yWEc4Qmt5dTlxcDV4cjA2TENIbTJyS3JyNmRDUVZXQVdEdDM4YktreUk0aG01UjU1QnJUeVJXUncyNUUvWGhRMFZLL2tRSWFvRmdIb2lqNHpIOW5sZWZ2TG5oWmQ1T0c0Ti9vTktqQSsvS25Famk3T0F4SllTWkdRZkY1NEdQMEExOFZxdTVVRmhQSjFGRUF2eWI0dEJ2bU8zNTRRVVMrOVE2Nmo8L1g1MDlDZXJ0aWZpY2F0ZT48L1g1MDlEYXRhPjwvS2V5SW5mbz48L1NpZ25hdHVyZT48Um9sZURlc2NyaXB0b3IgeHNpOnR5cGU9ImZlZDpTZWN1cml0eVRva2VuU2VydmljZVR5cGUiIHByb3RvY29sU3VwcG9ydEVudW1lcmF0aW9uPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9mZWRlcmF0aW9uLzIwMDcwNiIgeG1sbnM6eHNpPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxL1hNTFNjaGVtYS1pbnN0YW5jZSIgeG1sbnM6ZmVkPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9mZWRlcmF0aW9uLzIwMDcwNiI+PEtleURlc2NyaXB0b3IgdXNlPSJzaWduaW5nIj48S2V5SW5mbyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC8wOS94bWxkc2lnIyI+PFg1MDlEYXRhPjxYNTA5Q2VydGlmaWNhdGU+TUlJQzhEQ0NBZGlnQXdJQkFnSVFRMFZlWkt1UEtvSlBRaFo0aENpZHNEQU5CZ2txaGtpRzl3MEJBUXNGQURBME1USXdNQVlEVlFRREV5bE5hV055YjNOdlpuUWdRWHAxY21VZ1JtVmtaWEpoZEdWa0lGTlRUeUJEWlhKMGFXWnBZMkYwWlRBZUZ3MHhPREEwTVRVeE1USXpNek5hRncweU1UQTBNVFV4TVRJek16TmFNRFF4TWpBd0JnTlZCQU1US1UxcFkzSnZjMjltZENCQmVuVnlaU0JHWldSbGNtRjBaV1FnVTFOUElFTmxjblJwWm1sallYUmxNSUlCSWpBTkJna3Foa2lHOXcwQkFRRUZBQU9DQVE4QU1JSUJDZ0tDQVFFQTRVdWphR3Q4WFo4OXZ1dnlreVFXNVhvbi84Ui9pUHR6NGFiME0zdE1VdkdYejNVeHRXWlNFK1RHWHJ2M3dUdEswKzhGa015dUphSEZJcEsvNFVERmlGTXJCbHNHRnV2a1NzWnlWMjNmU0Y3elppeVRZNlQ3QTBwK2dzNTA1WEQ5R0FiOVZiZHdHRzArS0NWeWlzVlFnVjJJd0pnaXlocXdFQ29jd0JyYW43bnVLK1RFTkQybDJmOVlyeDVvUk1FTno3MHdseUgzNk9aQm10MGs1OTgvV2gwSERZTFplbzBkeVNXck53d2VZdlN4RTgvTWRtNDNYRXVTemJqVHpmc00wdlVSd0ZCU3JVTEVhRE8xL0lQMlVyN0JzZ0h3UkkveGZvcUltSzFLa3BVcTBBbGNUQWkzdjF1OXpDL3FMZ1B3QXlRSXZ3OVVDc2lyclBBMFkwWU9oUUlEQVFBQk1BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRRGNqb2pkR3ovQUlDampNMFo3bVlsZ1A1emJzYVE1ZEMyY2pmNERKcW1rbXNXdWZScEM0c2JzdWg4NzBjQ0JLY3V2aCtvR2l6QlFIclBtNFRoSXZmSWxLTDhYakxBWGJGdVJQb0hBZzA4c0xYZHZQVEJUTnZERjFNaG9xTnMyajZlRnEvZE51cXZlQkhyNUQ1dEtuVjJYQkdFSEU5UkU5V1RrWlFPYzBoSG1Dd01tY1lvclhHOEJreXU5cXA1eHIwNkxDSG0ycktycjZkQ1FWV0FXRHQzOGJLa3lJNGhtNVI1NUJyVHlSV1J3MjVFL1hoUTBWSy9rUUlhb0ZnSG9pajR6SDlubGVmdkxuaFpkNU9HNE4vb05LakErL0tuRWppN09BeEpZU1pHUWZGNTRHUDBBMThWcXU1VUZoUEoxRkVBdnliNHRCdm1PMzU0UVVTKzlRNjZqPC9YNTA5Q2VydGlmaWNhdGU+PC9YNTA5RGF0YT48L0tleUluZm8+PC9LZXlEZXNjcmlwdG9yPjxmZWQ6Q2xhaW1UeXBlc09mZmVyZWQ+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMueG1sc29hcC5vcmcvd3MvMjAwNS8wNS9pZGVudGl0eS9jbGFpbXMvbmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPk5hbWU8L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+VGhlIG11dGFibGUgZGlzcGxheSBuYW1lIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLnhtbHNvYXAub3JnL3dzLzIwMDUvMDUvaWRlbnRpdHkvY2xhaW1zL25hbWVpZGVudGlmaWVyIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+U3ViamVjdDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5BbiBpbW11dGFibGUsIGdsb2JhbGx5IHVuaXF1ZSwgbm9uLXJldXNhYmxlIGlkZW50aWZpZXIgb2YgdGhlIHVzZXIgdGhhdCBpcyB1bmlxdWUgdG8gdGhlIGFwcGxpY2F0aW9uIGZvciB3aGljaCBhIHRva2VuIGlzIGlzc3VlZC48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9naXZlbm5hbWUiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5HaXZlbiBOYW1lPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkZpcnN0IG5hbWUgb2YgdGhlIHVzZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMueG1sc29hcC5vcmcvd3MvMjAwNS8wNS9pZGVudGl0eS9jbGFpbXMvc3VybmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPlN1cm5hbWU8L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+TGFzdCBuYW1lIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL2Rpc3BsYXluYW1lIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+RGlzcGxheSBOYW1lPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkRpc3BsYXkgbmFtZSBvZiB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9uaWNrbmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPk5pY2sgTmFtZTwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5OaWNrIG5hbWUgb2YgdGhlIHVzZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9hdXRoZW50aWNhdGlvbmluc3RhbnQiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5BdXRoZW50aWNhdGlvbiBJbnN0YW50PC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlRoZSB0aW1lIChVVEMpIHdoZW4gdGhlIHVzZXIgaXMgYXV0aGVudGljYXRlZCB0byBXaW5kb3dzIEF6dXJlIEFjdGl2ZSBEaXJlY3RvcnkuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9hdXRoZW50aWNhdGlvbm1ldGhvZCIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkF1dGhlbnRpY2F0aW9uIE1ldGhvZDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5UaGUgbWV0aG9kIHRoYXQgV2luZG93cyBBenVyZSBBY3RpdmUgRGlyZWN0b3J5IHVzZXMgdG8gYXV0aGVudGljYXRlIHVzZXJzLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL29iamVjdGlkZW50aWZpZXIiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5PYmplY3RJZGVudGlmaWVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlByaW1hcnkgaWRlbnRpZmllciBmb3IgdGhlIHVzZXIgaW4gdGhlIGRpcmVjdG9yeS4gSW1tdXRhYmxlLCBnbG9iYWxseSB1bmlxdWUsIG5vbi1yZXVzYWJsZS48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRpZCIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPlRlbmFudElkPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPklkZW50aWZpZXIgZm9yIHRoZSB1c2VyJ3MgdGVuYW50LjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL2lkZW50aXR5cHJvdmlkZXIiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5JZGVudGl0eVByb3ZpZGVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPklkZW50aXR5IHByb3ZpZGVyIGZvciB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9lbWFpbGFkZHJlc3MiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5FbWFpbDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5FbWFpbCBhZGRyZXNzIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vd3MvMjAwOC8wNi9pZGVudGl0eS9jbGFpbXMvZ3JvdXBzIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+R3JvdXBzPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkdyb3VwcyBvZiB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9hY2Nlc3N0b2tlbiIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkV4dGVybmFsIEFjY2VzcyBUb2tlbjwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5BY2Nlc3MgdG9rZW4gaXNzdWVkIGJ5IGV4dGVybmFsIGlkZW50aXR5IHByb3ZpZGVyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vd3MvMjAwOC8wNi9pZGVudGl0eS9jbGFpbXMvZXhwaXJhdGlvbiIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkV4dGVybmFsIEFjY2VzcyBUb2tlbiBFeHBpcmF0aW9uPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlVUQyBleHBpcmF0aW9uIHRpbWUgb2YgYWNjZXNzIHRva2VuIGlzc3VlZCBieSBleHRlcm5hbCBpZGVudGl0eSBwcm92aWRlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9vcGVuaWQyX2lkIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+RXh0ZXJuYWwgT3BlbklEIDIuMCBJZGVudGlmaWVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPk9wZW5JRCAyLjAgaWRlbnRpZmllciBpc3N1ZWQgYnkgZXh0ZXJuYWwgaWRlbnRpdHkgcHJvdmlkZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS9jbGFpbXMvZ3JvdXBzLmxpbmsiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5Hcm91cHNPdmVyYWdlQ2xhaW08L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+SXNzdWVkIHdoZW4gbnVtYmVyIG9mIHVzZXIncyBncm91cCBjbGFpbXMgZXhjZWVkcyByZXR1cm4gbGltaXQuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9yb2xlIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+Um9sZSBDbGFpbTwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5Sb2xlcyB0aGF0IHRoZSB1c2VyIG9yIFNlcnZpY2UgUHJpbmNpcGFsIGlzIGF0dGFjaGVkIHRvPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy93aWRzIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+Um9sZVRlbXBsYXRlIElkIENsYWltPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlJvbGUgdGVtcGxhdGUgaWQgb2YgdGhlIEJ1aWx0LWluIERpcmVjdG9yeSBSb2xlcyB0aGF0IHRoZSB1c2VyIGlzIGEgbWVtYmVyIG9mPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PC9mZWQ6Q2xhaW1UeXBlc09mZmVyZWQ+PGZlZDpTZWN1cml0eVRva2VuU2VydmljZUVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpTZWN1cml0eVRva2VuU2VydmljZUVuZHBvaW50PjxmZWQ6UGFzc2l2ZVJlcXVlc3RvckVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpQYXNzaXZlUmVxdWVzdG9yRW5kcG9pbnQ+PC9Sb2xlRGVzY3JpcHRvcj48Um9sZURlc2NyaXB0b3IgeHNpOnR5cGU9ImZlZDpBcHBsaWNhdGlvblNlcnZpY2VUeXBlIiBwcm90b2NvbFN1cHBvcnRFbnVtZXJhdGlvbj0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvZmVkZXJhdGlvbi8yMDA3MDYiIHhtbG5zOnhzaT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS9YTUxTY2hlbWEtaW5zdGFuY2UiIHhtbG5zOmZlZD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvZmVkZXJhdGlvbi8yMDA3MDYiPjxLZXlEZXNjcmlwdG9yIHVzZT0ic2lnbmluZyI+PEtleUluZm8geG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjxYNTA5RGF0YT48WDUwOUNlcnRpZmljYXRlPk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2ajwvWDUwOUNlcnRpZmljYXRlPjwvWDUwOURhdGE+PC9LZXlJbmZvPjwvS2V5RGVzY3JpcHRvcj48ZmVkOlRhcmdldFNjb3Blcz48d3NhOkVuZHBvaW50UmVmZXJlbmNlIHhtbG5zOndzYT0iaHR0cDovL3d3dy53My5vcmcvMjAwNS8wOC9hZGRyZXNzaW5nIj48d3NhOkFkZHJlc3M+aHR0cHM6Ly9zdHMud2luZG93cy5uZXQvNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3Lzwvd3NhOkFkZHJlc3M+PC93c2E6RW5kcG9pbnRSZWZlcmVuY2U+PC9mZWQ6VGFyZ2V0U2NvcGVzPjxmZWQ6QXBwbGljYXRpb25TZXJ2aWNlRW5kcG9pbnQ+PHdzYTpFbmRwb2ludFJlZmVyZW5jZSB4bWxuczp3c2E9Imh0dHA6Ly93d3cudzMub3JnLzIwMDUvMDgvYWRkcmVzc2luZyI+PHdzYTpBZGRyZXNzPmh0dHBzOi8vbG9naW4ubWljcm9zb2Z0b25saW5lLmNvbS82MjFhYzEyZC00YWZiLTQ3OWMtOWMxNC0xM2U3Yjc0M2NkMDcvd3NmZWQ8L3dzYTpBZGRyZXNzPjwvd3NhOkVuZHBvaW50UmVmZXJlbmNlPjwvZmVkOkFwcGxpY2F0aW9uU2VydmljZUVuZHBvaW50PjxmZWQ6UGFzc2l2ZVJlcXVlc3RvckVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpQYXNzaXZlUmVxdWVzdG9yRW5kcG9pbnQ+PC9Sb2xlRGVzY3JpcHRvcj48SURQU1NPRGVzY3JpcHRvciBwcm90b2NvbFN1cHBvcnRFbnVtZXJhdGlvbj0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOnByb3RvY29sIj48S2V5RGVzY3JpcHRvciB1c2U9InNpZ25pbmciPjxLZXlJbmZvIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwLzA5L3htbGRzaWcjIj48WDUwOURhdGE+PFg1MDlDZXJ0aWZpY2F0ZT5NSUlDOERDQ0FkaWdBd0lCQWdJUVEwVmVaS3VQS29KUFFoWjRoQ2lkc0RBTkJna3Foa2lHOXcwQkFRc0ZBREEwTVRJd01BWURWUVFERXlsTmFXTnliM052Wm5RZ1FYcDFjbVVnUm1Wa1pYSmhkR1ZrSUZOVFR5QkRaWEowYVdacFkyRjBaVEFlRncweE9EQTBNVFV4TVRJek16TmFGdzB5TVRBME1UVXhNVEl6TXpOYU1EUXhNakF3QmdOVkJBTVRLVTFwWTNKdmMyOW1kQ0JCZW5WeVpTQkdaV1JsY21GMFpXUWdVMU5QSUVObGNuUnBabWxqWVhSbE1JSUJJakFOQmdrcWhraUc5dzBCQVFFRkFBT0NBUThBTUlJQkNnS0NBUUVBNFV1amFHdDhYWjg5dnV2eWt5UVc1WG9uLzhSL2lQdHo0YWIwTTN0TVV2R1h6M1V4dFdaU0UrVEdYcnYzd1R0SzArOEZrTXl1SmFIRklwSy80VURGaUZNckJsc0dGdXZrU3NaeVYyM2ZTRjd6Wml5VFk2VDdBMHArZ3M1MDVYRDlHQWI5VmJkd0dHMCtLQ1Z5aXNWUWdWMkl3SmdpeWhxd0VDb2N3QnJhbjdudUsrVEVORDJsMmY5WXJ4NW9STUVOejcwd2x5SDM2T1pCbXQwazU5OC9XaDBIRFlMWmVvMGR5U1dyTnd3ZVl2U3hFOC9NZG00M1hFdVN6YmpUemZzTTB2VVJ3RkJTclVMRWFETzEvSVAyVXI3QnNnSHdSSS94Zm9xSW1LMUtrcFVxMEFsY1RBaTN2MXU5ekMvcUxnUHdBeVFJdnc5VUNzaXJyUEEwWTBZT2hRSURBUUFCTUEwR0NTcUdTSWIzRFFFQkN3VUFBNElCQVFEY2pvamRHei9BSUNqak0wWjdtWWxnUDV6YnNhUTVkQzJjamY0REpxbWttc1d1ZlJwQzRzYnN1aDg3MGNDQktjdXZoK29HaXpCUUhyUG00VGhJdmZJbEtMOFhqTEFYYkZ1UlBvSEFnMDhzTFhkdlBUQlROdkRGMU1ob3FOczJqNmVGcS9kTnVxdmVCSHI1RDV0S25WMlhCR0VIRTlSRTlXVGtaUU9jMGhIbUN3TW1jWW9yWEc4Qmt5dTlxcDV4cjA2TENIbTJyS3JyNmRDUVZXQVdEdDM4YktreUk0aG01UjU1QnJUeVJXUncyNUUvWGhRMFZLL2tRSWFvRmdIb2lqNHpIOW5sZWZ2TG5oWmQ1T0c0Ti9vTktqQSsvS25Famk3T0F4SllTWkdRZkY1NEdQMEExOFZxdTVVRmhQSjFGRUF2eWI0dEJ2bU8zNTRRVVMrOVE2Nmo8L1g1MDlDZXJ0aWZpY2F0ZT48L1g1MDlEYXRhPjwvS2V5SW5mbz48L0tleURlc2NyaXB0b3I+PFNpbmdsZUxvZ291dFNlcnZpY2UgQmluZGluZz0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOmJpbmRpbmdzOkhUVFAtUmVkaXJlY3QiIExvY2F0aW9uPSJodHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3NhbWwyIiAvPjxTaW5nbGVTaWduT25TZXJ2aWNlIEJpbmRpbmc9InVybjpvYXNpczpuYW1lczp0YzpTQU1MOjIuMDpiaW5kaW5nczpIVFRQLVJlZGlyZWN0IiBMb2NhdGlvbj0iaHR0cHM6Ly9sb2dpbi5taWNyb3NvZnRvbmxpbmUuY29tLzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy9zYW1sMiIgLz48U2luZ2xlU2lnbk9uU2VydmljZSBCaW5kaW5nPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6YmluZGluZ3M6SFRUUC1QT1NUIiBMb2NhdGlvbj0iaHR0cHM6Ly9sb2dpbi5taWNyb3NvZnRvbmxpbmUuY29tLzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy9zYW1sMiIgLz48L0lEUFNTT0Rlc2NyaXB0b3I+PC9FbnRpdHlEZXNjcmlwdG9yPg==\",\n    \"received-identifier\" : \"https://sts.windows.net/621ac12d-4afb-479c-9c14-13e7b888cd07/\",\n    \"login-url\" : \"https://login.microsoftonline.com/621ac12d-4afb-479c-9c14-13e7b743cd07/saml2\",\n    \"base64-certificate\" : \"LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2agotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0t\"\n  }, {\n    \"uid\" : \"2e771118-7a1e-4076-a50d-30233db2552d\",\n    \"name\" : \"TestIdp_Clone\",\n    \"type\" : \"identity-provider\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1740375529621,\n        \"iso-8601\" : \"2025-02-24T07:38+0200\"\n      },\n      \"last-modifier\" : \"WEB_API\",\n      \"creation-time\" : {\n        \"posix\" : 1740375529621,\n        \"iso-8601\" : \"2025-02-24T07:38+0200\"\n      },\n      \"creator\" : \"WEB_API\"\n    },\n    \"available-actions\" : {\n      \"edit\" : \"true\",\n      \"delete\" : \"true\",\n      \"clone\" : \"true\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"Objects/AuthenticationServer\",\n    \"usage\" : \"managing_administrator_access\",\n    \"gateway\" : {\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c471\",\n      \"name\" : \"None\",\n      \"type\" : \"Global\",\n      \"domain\" : {\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\",\n        \"domain-type\" : \"data domain\"\n      },\n      \"color\" : \"none\",\n      \"meta-info\" : {\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1738588299506,\n          \"iso-8601\" : \"2025-02-03T15:11+0200\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1738588299506,\n          \"iso-8601\" : \"2025-02-03T15:11+0200\"\n        },\n        \"creator\" : \"System\"\n      },\n      \"tags\" : [ ],\n      \"icon\" : \"General/globalsNone\",\n      \"comments\" : \"None\",\n      \"customFields\" : null\n    },\n    \"service\" : \"none\",\n    \"required-identifier\" : \"https://mgmt-sp-0e4cae10-43f9-4b66-87a8-931d5285df11.local/cpmws/saml/acs/id/0e4cae10-43f9-4b66-87a8-931d5285df11\",\n    \"reply-urls\" : [ \"https://172.23.48.144/cpmws/saml/acs/sso\" ],\n    \"data-receiving\" : \"metadata_file\",\n    \"base64-metadata-file\" : \"PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48RW50aXR5RGVzY3JpcHRvciBJRD0iXzkwMzU3YWM3LWQ4N2ItNDczZi05Njg2LTEzZjEyOTcwYWJhYiIgZW50aXR5SUQ9Imh0dHBzOi8vc3RzLndpbmRvd3MubmV0LzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy8iIHhtbG5zPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6bWV0YWRhdGEiPjxTaWduYXR1cmUgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjxTaWduZWRJbmZvPjxDYW5vbmljYWxpemF0aW9uTWV0aG9kIEFsZ29yaXRobT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS8xMC94bWwtZXhjLWMxNG4jIiAvPjxTaWduYXR1cmVNZXRob2QgQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNyc2Etc2hhMjU2IiAvPjxSZWZlcmVuY2UgVVJJPSIjXzkwMzU3YWM3LWQ4N2ItNDczZi05Njg2LTEzZjEyOTcwYWJhYiI+PFRyYW5zZm9ybXM+PFRyYW5zZm9ybSBBbGdvcml0aG09Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyNlbnZlbG9wZWQtc2lnbmF0dXJlIiAvPjxUcmFuc2Zvcm0gQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzEwL3htbC1leGMtYzE0biMiIC8+PC9UcmFuc2Zvcm1zPjxEaWdlc3RNZXRob2QgQWxnb3JpdGhtPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGVuYyNzaGEyNTYiIC8+PERpZ2VzdFZhbHVlPnBPazZnV2QyakNCTzlIb2k4dlp3c3Nqc0VEdE0vYzhKN0E3QmRCUGsvMGc9PC9EaWdlc3RWYWx1ZT48L1JlZmVyZW5jZT48L1NpZ25lZEluZm8+PFNpZ25hdHVyZVZhbHVlPnJIMXVnV0tkbUpCR0c0ckJJcUVFbUhGeEpMVHBRZGp1eUJKV01DTEtMaDNxL250Qksyd2JRQ1dSV0d2MjM0K2xRMWtXNVdjdDFmQlNUcDI1VDU2dis2V21GZnZad3dQb3p4U3F6cURrTzdhclA0Qm50MEh6a0QvRm1MQVZEdE83d3RRVzlsK3R2QkhMT241VkVDTzJ6RVU0anBSTXNnWDFkMUZIckk2M3o4dDZLcm13Q3ljN0hVTGk3WXlaREc0ckt1aUFIU2ZuNWpkRExLV2VVQnh4YWZtd2V1Q1BzVGpEbGcrNnQrYVFqNDl2cjR3N0htcmtCZmNTaXU0VCtYbnBLSG9KaW5TU2YrWFJ1eW1razBiQnJXdVlnQit1YWZmMmEydXV4RFB1ZEtHUXFoRSs5MnUrZnpJbWp0ZjRpM3pNYThOSGVRdDg5ZXBITVluYTNaemE1dz09PC9TaWduYXR1cmVWYWx1ZT48S2V5SW5mbz48WDUwOURhdGE+PFg1MDlDZXJ0aWZpY2F0ZT5NSUlDOERDQ0FkaWdBd0lCQWdJUVEwVmVaS3VQS29KUFFoWjRoQ2lkc0RBTkJna3Foa2lHOXcwQkFRc0ZBREEwTVRJd01BWURWUVFERXlsTmFXTnliM052Wm5RZ1FYcDFjbVVnUm1Wa1pYSmhkR1ZrSUZOVFR5QkRaWEowYVdacFkyRjBaVEFlRncweE9EQTBNVFV4TVRJek16TmFGdzB5TVRBME1UVXhNVEl6TXpOYU1EUXhNakF3QmdOVkJBTVRLVTFwWTNKdmMyOW1kQ0JCZW5WeVpTQkdaV1JsY21GMFpXUWdVMU5QSUVObGNuUnBabWxqWVhSbE1JSUJJakFOQmdrcWhraUc5dzBCQVFFRkFBT0NBUThBTUlJQkNnS0NBUUVBNFV1amFHdDhYWjg5dnV2eWt5UVc1WG9uLzhSL2lQdHo0YWIwTTN0TVV2R1h6M1V4dFdaU0UrVEdYcnYzd1R0SzArOEZrTXl1SmFIRklwSy80VURGaUZNckJsc0dGdXZrU3NaeVYyM2ZTRjd6Wml5VFk2VDdBMHArZ3M1MDVYRDlHQWI5VmJkd0dHMCtLQ1Z5aXNWUWdWMkl3SmdpeWhxd0VDb2N3QnJhbjdudUsrVEVORDJsMmY5WXJ4NW9STUVOejcwd2x5SDM2T1pCbXQwazU5OC9XaDBIRFlMWmVvMGR5U1dyTnd3ZVl2U3hFOC9NZG00M1hFdVN6YmpUemZzTTB2VVJ3RkJTclVMRWFETzEvSVAyVXI3QnNnSHdSSS94Zm9xSW1LMUtrcFVxMEFsY1RBaTN2MXU5ekMvcUxnUHdBeVFJdnc5VUNzaXJyUEEwWTBZT2hRSURBUUFCTUEwR0NTcUdTSWIzRFFFQkN3VUFBNElCQVFEY2pvamRHei9BSUNqak0wWjdtWWxnUDV6YnNhUTVkQzJjamY0REpxbWttc1d1ZlJwQzRzYnN1aDg3MGNDQktjdXZoK29HaXpCUUhyUG00VGhJdmZJbEtMOFhqTEFYYkZ1UlBvSEFnMDhzTFhkdlBUQlROdkRGMU1ob3FOczJqNmVGcS9kTnVxdmVCSHI1RDV0S25WMlhCR0VIRTlSRTlXVGtaUU9jMGhIbUN3TW1jWW9yWEc4Qmt5dTlxcDV4cjA2TENIbTJyS3JyNmRDUVZXQVdEdDM4YktreUk0aG01UjU1QnJUeVJXUncyNUUvWGhRMFZLL2tRSWFvRmdIb2lqNHpIOW5sZWZ2TG5oWmQ1T0c0Ti9vTktqQSsvS25Famk3T0F4SllTWkdRZkY1NEdQMEExOFZxdTVVRmhQSjFGRUF2eWI0dEJ2bU8zNTRRVVMrOVE2Nmo8L1g1MDlDZXJ0aWZpY2F0ZT48L1g1MDlEYXRhPjwvS2V5SW5mbz48L1NpZ25hdHVyZT48Um9sZURlc2NyaXB0b3IgeHNpOnR5cGU9ImZlZDpTZWN1cml0eVRva2VuU2VydmljZVR5cGUiIHByb3RvY29sU3VwcG9ydEVudW1lcmF0aW9uPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9mZWRlcmF0aW9uLzIwMDcwNiIgeG1sbnM6eHNpPSJodHRwOi8vd3d3LnczLm9yZy8yMDAxL1hNTFNjaGVtYS1pbnN0YW5jZSIgeG1sbnM6ZmVkPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9mZWRlcmF0aW9uLzIwMDcwNiI+PEtleURlc2NyaXB0b3IgdXNlPSJzaWduaW5nIj48S2V5SW5mbyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC8wOS94bWxkc2lnIyI+PFg1MDlEYXRhPjxYNTA5Q2VydGlmaWNhdGU+TUlJQzhEQ0NBZGlnQXdJQkFnSVFRMFZlWkt1UEtvSlBRaFo0aENpZHNEQU5CZ2txaGtpRzl3MEJBUXNGQURBME1USXdNQVlEVlFRREV5bE5hV055YjNOdlpuUWdRWHAxY21VZ1JtVmtaWEpoZEdWa0lGTlRUeUJEWlhKMGFXWnBZMkYwWlRBZUZ3MHhPREEwTVRVeE1USXpNek5hRncweU1UQTBNVFV4TVRJek16TmFNRFF4TWpBd0JnTlZCQU1US1UxcFkzSnZjMjltZENCQmVuVnlaU0JHWldSbGNtRjBaV1FnVTFOUElFTmxjblJwWm1sallYUmxNSUlCSWpBTkJna3Foa2lHOXcwQkFRRUZBQU9DQVE4QU1JSUJDZ0tDQVFFQTRVdWphR3Q4WFo4OXZ1dnlreVFXNVhvbi84Ui9pUHR6NGFiME0zdE1VdkdYejNVeHRXWlNFK1RHWHJ2M3dUdEswKzhGa015dUphSEZJcEsvNFVERmlGTXJCbHNHRnV2a1NzWnlWMjNmU0Y3elppeVRZNlQ3QTBwK2dzNTA1WEQ5R0FiOVZiZHdHRzArS0NWeWlzVlFnVjJJd0pnaXlocXdFQ29jd0JyYW43bnVLK1RFTkQybDJmOVlyeDVvUk1FTno3MHdseUgzNk9aQm10MGs1OTgvV2gwSERZTFplbzBkeVNXck53d2VZdlN4RTgvTWRtNDNYRXVTemJqVHpmc00wdlVSd0ZCU3JVTEVhRE8xL0lQMlVyN0JzZ0h3UkkveGZvcUltSzFLa3BVcTBBbGNUQWkzdjF1OXpDL3FMZ1B3QXlRSXZ3OVVDc2lyclBBMFkwWU9oUUlEQVFBQk1BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRRGNqb2pkR3ovQUlDampNMFo3bVlsZ1A1emJzYVE1ZEMyY2pmNERKcW1rbXNXdWZScEM0c2JzdWg4NzBjQ0JLY3V2aCtvR2l6QlFIclBtNFRoSXZmSWxLTDhYakxBWGJGdVJQb0hBZzA4c0xYZHZQVEJUTnZERjFNaG9xTnMyajZlRnEvZE51cXZlQkhyNUQ1dEtuVjJYQkdFSEU5UkU5V1RrWlFPYzBoSG1Dd01tY1lvclhHOEJreXU5cXA1eHIwNkxDSG0ycktycjZkQ1FWV0FXRHQzOGJLa3lJNGhtNVI1NUJyVHlSV1J3MjVFL1hoUTBWSy9rUUlhb0ZnSG9pajR6SDlubGVmdkxuaFpkNU9HNE4vb05LakErL0tuRWppN09BeEpZU1pHUWZGNTRHUDBBMThWcXU1VUZoUEoxRkVBdnliNHRCdm1PMzU0UVVTKzlRNjZqPC9YNTA5Q2VydGlmaWNhdGU+PC9YNTA5RGF0YT48L0tleUluZm8+PC9LZXlEZXNjcmlwdG9yPjxmZWQ6Q2xhaW1UeXBlc09mZmVyZWQ+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMueG1sc29hcC5vcmcvd3MvMjAwNS8wNS9pZGVudGl0eS9jbGFpbXMvbmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPk5hbWU8L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+VGhlIG11dGFibGUgZGlzcGxheSBuYW1lIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLnhtbHNvYXAub3JnL3dzLzIwMDUvMDUvaWRlbnRpdHkvY2xhaW1zL25hbWVpZGVudGlmaWVyIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+U3ViamVjdDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5BbiBpbW11dGFibGUsIGdsb2JhbGx5IHVuaXF1ZSwgbm9uLXJldXNhYmxlIGlkZW50aWZpZXIgb2YgdGhlIHVzZXIgdGhhdCBpcyB1bmlxdWUgdG8gdGhlIGFwcGxpY2F0aW9uIGZvciB3aGljaCBhIHRva2VuIGlzIGlzc3VlZC48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9naXZlbm5hbWUiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5HaXZlbiBOYW1lPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkZpcnN0IG5hbWUgb2YgdGhlIHVzZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMueG1sc29hcC5vcmcvd3MvMjAwNS8wNS9pZGVudGl0eS9jbGFpbXMvc3VybmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPlN1cm5hbWU8L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+TGFzdCBuYW1lIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL2Rpc3BsYXluYW1lIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+RGlzcGxheSBOYW1lPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkRpc3BsYXkgbmFtZSBvZiB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9uaWNrbmFtZSIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPk5pY2sgTmFtZTwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5OaWNrIG5hbWUgb2YgdGhlIHVzZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9hdXRoZW50aWNhdGlvbmluc3RhbnQiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5BdXRoZW50aWNhdGlvbiBJbnN0YW50PC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlRoZSB0aW1lIChVVEMpIHdoZW4gdGhlIHVzZXIgaXMgYXV0aGVudGljYXRlZCB0byBXaW5kb3dzIEF6dXJlIEFjdGl2ZSBEaXJlY3RvcnkuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9hdXRoZW50aWNhdGlvbm1ldGhvZCIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkF1dGhlbnRpY2F0aW9uIE1ldGhvZDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5UaGUgbWV0aG9kIHRoYXQgV2luZG93cyBBenVyZSBBY3RpdmUgRGlyZWN0b3J5IHVzZXMgdG8gYXV0aGVudGljYXRlIHVzZXJzLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL29iamVjdGlkZW50aWZpZXIiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5PYmplY3RJZGVudGlmaWVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlByaW1hcnkgaWRlbnRpZmllciBmb3IgdGhlIHVzZXIgaW4gdGhlIGRpcmVjdG9yeS4gSW1tdXRhYmxlLCBnbG9iYWxseSB1bmlxdWUsIG5vbi1yZXVzYWJsZS48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy90ZW5hbnRpZCIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPlRlbmFudElkPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPklkZW50aWZpZXIgZm9yIHRoZSB1c2VyJ3MgdGVuYW50LjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vaWRlbnRpdHkvY2xhaW1zL2lkZW50aXR5cHJvdmlkZXIiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5JZGVudGl0eVByb3ZpZGVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPklkZW50aXR5IHByb3ZpZGVyIGZvciB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9lbWFpbGFkZHJlc3MiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5FbWFpbDwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5FbWFpbCBhZGRyZXNzIG9mIHRoZSB1c2VyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vd3MvMjAwOC8wNi9pZGVudGl0eS9jbGFpbXMvZ3JvdXBzIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+R3JvdXBzPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPkdyb3VwcyBvZiB0aGUgdXNlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9hY2Nlc3N0b2tlbiIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkV4dGVybmFsIEFjY2VzcyBUb2tlbjwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5BY2Nlc3MgdG9rZW4gaXNzdWVkIGJ5IGV4dGVybmFsIGlkZW50aXR5IHByb3ZpZGVyLjwvYXV0aDpEZXNjcmlwdGlvbj48L2F1dGg6Q2xhaW1UeXBlPjxhdXRoOkNsYWltVHlwZSBVcmk9Imh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vd3MvMjAwOC8wNi9pZGVudGl0eS9jbGFpbXMvZXhwaXJhdGlvbiIgeG1sbnM6YXV0aD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvYXV0aG9yaXphdGlvbi8yMDA3MDYiPjxhdXRoOkRpc3BsYXlOYW1lPkV4dGVybmFsIEFjY2VzcyBUb2tlbiBFeHBpcmF0aW9uPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlVUQyBleHBpcmF0aW9uIHRpbWUgb2YgYWNjZXNzIHRva2VuIGlzc3VlZCBieSBleHRlcm5hbCBpZGVudGl0eSBwcm92aWRlci48L2F1dGg6RGVzY3JpcHRpb24+PC9hdXRoOkNsYWltVHlwZT48YXV0aDpDbGFpbVR5cGUgVXJpPSJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL2lkZW50aXR5L2NsYWltcy9vcGVuaWQyX2lkIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+RXh0ZXJuYWwgT3BlbklEIDIuMCBJZGVudGlmaWVyPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPk9wZW5JRCAyLjAgaWRlbnRpZmllciBpc3N1ZWQgYnkgZXh0ZXJuYWwgaWRlbnRpdHkgcHJvdmlkZXIuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS9jbGFpbXMvZ3JvdXBzLmxpbmsiIHhtbG5zOmF1dGg9Imh0dHA6Ly9kb2NzLm9hc2lzLW9wZW4ub3JnL3dzZmVkL2F1dGhvcml6YXRpb24vMjAwNzA2Ij48YXV0aDpEaXNwbGF5TmFtZT5Hcm91cHNPdmVyYWdlQ2xhaW08L2F1dGg6RGlzcGxheU5hbWU+PGF1dGg6RGVzY3JpcHRpb24+SXNzdWVkIHdoZW4gbnVtYmVyIG9mIHVzZXIncyBncm91cCBjbGFpbXMgZXhjZWVkcyByZXR1cm4gbGltaXQuPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy9yb2xlIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+Um9sZSBDbGFpbTwvYXV0aDpEaXNwbGF5TmFtZT48YXV0aDpEZXNjcmlwdGlvbj5Sb2xlcyB0aGF0IHRoZSB1c2VyIG9yIFNlcnZpY2UgUHJpbmNpcGFsIGlzIGF0dGFjaGVkIHRvPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PGF1dGg6Q2xhaW1UeXBlIFVyaT0iaHR0cDovL3NjaGVtYXMubWljcm9zb2Z0LmNvbS93cy8yMDA4LzA2L2lkZW50aXR5L2NsYWltcy93aWRzIiB4bWxuczphdXRoPSJodHRwOi8vZG9jcy5vYXNpcy1vcGVuLm9yZy93c2ZlZC9hdXRob3JpemF0aW9uLzIwMDcwNiI+PGF1dGg6RGlzcGxheU5hbWU+Um9sZVRlbXBsYXRlIElkIENsYWltPC9hdXRoOkRpc3BsYXlOYW1lPjxhdXRoOkRlc2NyaXB0aW9uPlJvbGUgdGVtcGxhdGUgaWQgb2YgdGhlIEJ1aWx0LWluIERpcmVjdG9yeSBSb2xlcyB0aGF0IHRoZSB1c2VyIGlzIGEgbWVtYmVyIG9mPC9hdXRoOkRlc2NyaXB0aW9uPjwvYXV0aDpDbGFpbVR5cGU+PC9mZWQ6Q2xhaW1UeXBlc09mZmVyZWQ+PGZlZDpTZWN1cml0eVRva2VuU2VydmljZUVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpTZWN1cml0eVRva2VuU2VydmljZUVuZHBvaW50PjxmZWQ6UGFzc2l2ZVJlcXVlc3RvckVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpQYXNzaXZlUmVxdWVzdG9yRW5kcG9pbnQ+PC9Sb2xlRGVzY3JpcHRvcj48Um9sZURlc2NyaXB0b3IgeHNpOnR5cGU9ImZlZDpBcHBsaWNhdGlvblNlcnZpY2VUeXBlIiBwcm90b2NvbFN1cHBvcnRFbnVtZXJhdGlvbj0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvZmVkZXJhdGlvbi8yMDA3MDYiIHhtbG5zOnhzaT0iaHR0cDovL3d3dy53My5vcmcvMjAwMS9YTUxTY2hlbWEtaW5zdGFuY2UiIHhtbG5zOmZlZD0iaHR0cDovL2RvY3Mub2FzaXMtb3Blbi5vcmcvd3NmZWQvZmVkZXJhdGlvbi8yMDA3MDYiPjxLZXlEZXNjcmlwdG9yIHVzZT0ic2lnbmluZyI+PEtleUluZm8geG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvMDkveG1sZHNpZyMiPjxYNTA5RGF0YT48WDUwOUNlcnRpZmljYXRlPk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2ajwvWDUwOUNlcnRpZmljYXRlPjwvWDUwOURhdGE+PC9LZXlJbmZvPjwvS2V5RGVzY3JpcHRvcj48ZmVkOlRhcmdldFNjb3Blcz48d3NhOkVuZHBvaW50UmVmZXJlbmNlIHhtbG5zOndzYT0iaHR0cDovL3d3dy53My5vcmcvMjAwNS8wOC9hZGRyZXNzaW5nIj48d3NhOkFkZHJlc3M+aHR0cHM6Ly9zdHMud2luZG93cy5uZXQvNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3Lzwvd3NhOkFkZHJlc3M+PC93c2E6RW5kcG9pbnRSZWZlcmVuY2U+PC9mZWQ6VGFyZ2V0U2NvcGVzPjxmZWQ6QXBwbGljYXRpb25TZXJ2aWNlRW5kcG9pbnQ+PHdzYTpFbmRwb2ludFJlZmVyZW5jZSB4bWxuczp3c2E9Imh0dHA6Ly93d3cudzMub3JnLzIwMDUvMDgvYWRkcmVzc2luZyI+PHdzYTpBZGRyZXNzPmh0dHBzOi8vbG9naW4ubWljcm9zb2Z0b25saW5lLmNvbS82MjFhYzEyZC00YWZiLTQ3OWMtOWMxNC0xM2U3Yjc0M2NkMDcvd3NmZWQ8L3dzYTpBZGRyZXNzPjwvd3NhOkVuZHBvaW50UmVmZXJlbmNlPjwvZmVkOkFwcGxpY2F0aW9uU2VydmljZUVuZHBvaW50PjxmZWQ6UGFzc2l2ZVJlcXVlc3RvckVuZHBvaW50Pjx3c2E6RW5kcG9pbnRSZWZlcmVuY2UgeG1sbnM6d3NhPSJodHRwOi8vd3d3LnczLm9yZy8yMDA1LzA4L2FkZHJlc3NpbmciPjx3c2E6QWRkcmVzcz5odHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3dzZmVkPC93c2E6QWRkcmVzcz48L3dzYTpFbmRwb2ludFJlZmVyZW5jZT48L2ZlZDpQYXNzaXZlUmVxdWVzdG9yRW5kcG9pbnQ+PC9Sb2xlRGVzY3JpcHRvcj48SURQU1NPRGVzY3JpcHRvciBwcm90b2NvbFN1cHBvcnRFbnVtZXJhdGlvbj0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOnByb3RvY29sIj48S2V5RGVzY3JpcHRvciB1c2U9InNpZ25pbmciPjxLZXlJbmZvIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwLzA5L3htbGRzaWcjIj48WDUwOURhdGE+PFg1MDlDZXJ0aWZpY2F0ZT5NSUlDOERDQ0FkaWdBd0lCQWdJUVEwVmVaS3VQS29KUFFoWjRoQ2lkc0RBTkJna3Foa2lHOXcwQkFRc0ZBREEwTVRJd01BWURWUVFERXlsTmFXTnliM052Wm5RZ1FYcDFjbVVnUm1Wa1pYSmhkR1ZrSUZOVFR5QkRaWEowYVdacFkyRjBaVEFlRncweE9EQTBNVFV4TVRJek16TmFGdzB5TVRBME1UVXhNVEl6TXpOYU1EUXhNakF3QmdOVkJBTVRLVTFwWTNKdmMyOW1kQ0JCZW5WeVpTQkdaV1JsY21GMFpXUWdVMU5QSUVObGNuUnBabWxqWVhSbE1JSUJJakFOQmdrcWhraUc5dzBCQVFFRkFBT0NBUThBTUlJQkNnS0NBUUVBNFV1amFHdDhYWjg5dnV2eWt5UVc1WG9uLzhSL2lQdHo0YWIwTTN0TVV2R1h6M1V4dFdaU0UrVEdYcnYzd1R0SzArOEZrTXl1SmFIRklwSy80VURGaUZNckJsc0dGdXZrU3NaeVYyM2ZTRjd6Wml5VFk2VDdBMHArZ3M1MDVYRDlHQWI5VmJkd0dHMCtLQ1Z5aXNWUWdWMkl3SmdpeWhxd0VDb2N3QnJhbjdudUsrVEVORDJsMmY5WXJ4NW9STUVOejcwd2x5SDM2T1pCbXQwazU5OC9XaDBIRFlMWmVvMGR5U1dyTnd3ZVl2U3hFOC9NZG00M1hFdVN6YmpUemZzTTB2VVJ3RkJTclVMRWFETzEvSVAyVXI3QnNnSHdSSS94Zm9xSW1LMUtrcFVxMEFsY1RBaTN2MXU5ekMvcUxnUHdBeVFJdnc5VUNzaXJyUEEwWTBZT2hRSURBUUFCTUEwR0NTcUdTSWIzRFFFQkN3VUFBNElCQVFEY2pvamRHei9BSUNqak0wWjdtWWxnUDV6YnNhUTVkQzJjamY0REpxbWttc1d1ZlJwQzRzYnN1aDg3MGNDQktjdXZoK29HaXpCUUhyUG00VGhJdmZJbEtMOFhqTEFYYkZ1UlBvSEFnMDhzTFhkdlBUQlROdkRGMU1ob3FOczJqNmVGcS9kTnVxdmVCSHI1RDV0S25WMlhCR0VIRTlSRTlXVGtaUU9jMGhIbUN3TW1jWW9yWEc4Qmt5dTlxcDV4cjA2TENIbTJyS3JyNmRDUVZXQVdEdDM4YktreUk0aG01UjU1QnJUeVJXUncyNUUvWGhRMFZLL2tRSWFvRmdIb2lqNHpIOW5sZWZ2TG5oWmQ1T0c0Ti9vTktqQSsvS25Famk3T0F4SllTWkdRZkY1NEdQMEExOFZxdTVVRmhQSjFGRUF2eWI0dEJ2bU8zNTRRVVMrOVE2Nmo8L1g1MDlDZXJ0aWZpY2F0ZT48L1g1MDlEYXRhPjwvS2V5SW5mbz48L0tleURlc2NyaXB0b3I+PFNpbmdsZUxvZ291dFNlcnZpY2UgQmluZGluZz0idXJuOm9hc2lzOm5hbWVzOnRjOlNBTUw6Mi4wOmJpbmRpbmdzOkhUVFAtUmVkaXJlY3QiIExvY2F0aW9uPSJodHRwczovL2xvZ2luLm1pY3Jvc29mdG9ubGluZS5jb20vNjIxYWMxMmQtNGFmYi00NzljLTljMTQtMTNlN2I3NDNjZDA3L3NhbWwyIiAvPjxTaW5nbGVTaWduT25TZXJ2aWNlIEJpbmRpbmc9InVybjpvYXNpczpuYW1lczp0YzpTQU1MOjIuMDpiaW5kaW5nczpIVFRQLVJlZGlyZWN0IiBMb2NhdGlvbj0iaHR0cHM6Ly9sb2dpbi5taWNyb3NvZnRvbmxpbmUuY29tLzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy9zYW1sMiIgLz48U2luZ2xlU2lnbk9uU2VydmljZSBCaW5kaW5nPSJ1cm46b2FzaXM6bmFtZXM6dGM6U0FNTDoyLjA6YmluZGluZ3M6SFRUUC1QT1NUIiBMb2NhdGlvbj0iaHR0cHM6Ly9sb2dpbi5taWNyb3NvZnRvbmxpbmUuY29tLzYyMWFjMTJkLTRhZmItNDc5Yy05YzE0LTEzZTdiNzQzY2QwNy9zYW1sMiIgLz48L0lEUFNTT0Rlc2NyaXB0b3I+PC9FbnRpdHlEZXNjcmlwdG9yPg==\",\n    \"received-identifier\" : \"https://sts.windows.net/621ac12d-4afb-479c-9c14-13e7b743cd07/\",\n    \"login-url\" : \"https://login.microsoftonline.com/621ac12d-4afb-479c-9c14-13e7b743cd07/saml2\",\n    \"base64-certificate\" : \"LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2agotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0t\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:25.284552",
    "source_file": "show-identity-providers.html"
  }
}
```