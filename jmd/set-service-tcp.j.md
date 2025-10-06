# set-service-tcp

```json
{
  "command": "set-service-tcp",
  "description": "Edit existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-service-tcp",
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
        "name": "aggressive-aging",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "default-timeout",
        "description": "Default aggressive aging timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "enable",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "timeout",
        "description": "Aggressive aging timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "use-default-timeout",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keep-connections-open-after-policy-installation",
        "description": "Keep connections open after policy has been installed even if they are not allowed under the new policy. This overrides the settings in the Connection Persistence page. If you change this property, the change will not affect open connections, but only future connections.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "match-by-protocol-signature",
        "description": "A value of true enables matching by the selected protocol's signature - the signature identifies the protocol as genuine. Select this option to limit the port to the specified protocol. If the selected protocol does not support matching by signature, this field cannot be set to true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "match-for-any",
        "description": "Indicates whether this service is used when 'Any' is set as the rule's service and there are several service objects with the same source port and protocol.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-default-settings",
        "description": "Indicates whether this service is a Data Domain service which has been overridden.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "port",
        "description": "The number of the port used to provide this service. To specify a port range, place a hyphen between the lowest and highest port numbers, for example 44-55.",
        "type": "string",
        "required": false
      },
      {
        "name": "protocol",
        "description": "Protocol name or uid. Select the protocol type associated with the service, and by implication, the management server (if any) that enforces Content Security and Authentication for the service. Selecting a Protocol Type invokes the specific protocol handlers for each protocol type, thus enabling higher level of security by parsing the protocol, and higher level of connectivity by tracking dynamic actions (such as opening of ports).To remove, set value to 'none'.",
        "type": "string",
        "required": false
      },
      {
        "name": "session-timeout",
        "description": "Time (in seconds) before the session times out.",
        "type": "integer",
        "required": false
      },
      {
        "name": "source-port",
        "description": "Port number for the client side service. If specified, only those Source port Numbers will be Accepted, Dropped, or Rejected during packet inspection. Otherwise, the source port is not inspected.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-default-session-timeout",
        "description": "Use default virtual session timeout.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-tcp-resource",
        "description": "Enable for tcp resource.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "sync-connections-on-cluster",
        "description": "Enables state-synchronized High Availability or Load Sharing on a ClusterXL or OPSEC-certified cluster.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-delayed-sync",
        "description": "Enable this option to delay notifying the Security Gateway about a connection, so that the connection will only be synchronized if it still exists x seconds after the connection is initiated. Relevant only for Clusters using an acceleration device supporting this feature.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "delayed-sync-value",
        "description": "Specify the delay (in seconds) in which a synchronization will start after connection initiation.",
        "type": "integer",
        "required": false,
        "default": "30"
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
        "name": "aggressive-aging",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "default-timeout",
        "description": "Default aggressive aging timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "enable",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "timeout",
        "description": "Aggressive aging timeout in seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "use-default-timeout",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "groups",
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
        "name": "keep-connections-open-after-policy-installation",
        "description": "Keep connections open after policy has been installed even if they are not allowed under the new policy. This overrides the settings in the Connection Persistence page. If you change this property, the change will not affect open connections, but only future connections.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "match-by-protocol-signature",
        "description": "A value of true enables matching by the selected protocol's signature - The signature identifies the protocol as genuine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "match-for-any",
        "description": "Indicates whether this service is used when 'Any' is set as the rule's service and there are several service objects with the same source port and protocol.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "override-default-settings",
        "description": "Indicates whether this service is a Data Domain service which has been overridden.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "port",
        "description": "The number of the port used to provide this service.",
        "type": "string",
        "required": false
      },
      {
        "name": "protocol",
        "description": "The protocol type associated with the service, and by implication, the management server (if any) that enforces Content Security and Authentication for the service.",
        "type": "string",
        "required": false
      },
      {
        "name": "session-timeout",
        "description": "Time (in seconds) before the session times out.",
        "type": "integer",
        "required": false
      },
      {
        "name": "source-port",
        "description": "Port number for the client side service. If specified, only those Source port Numbers will be Accepted, Dropped, or Rejected during packet inspection. Otherwise, the source port is not inspected.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-default-session-timeout",
        "description": "Use default virtual session timeout.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-tcp-resource",
        "description": "Enable for tcp resource.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sync-connections-on-cluster",
        "description": "Enables state-synchronized High Availability or Load Sharing on a ClusterXL or OPSEC-certified cluster.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-delayed-sync",
        "description": "Enable this option to delay notifying the Security Gateway about a connection, so that the connection will only be synchronized if it still exists x seconds after the connection is initiated. Relevant only for Clusters using an acceleration device supporting this feature.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delayed-sync-value",
        "description": "Specify the delay (in seconds) in which a synchronization will start after connection initiation.",
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
    "set-service-tcp": {
      "description": "",
      "request": "POST {{server}}/set-service-tcp\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"New_TCP_Service_1\",\n  \"new-name\" : \"New_TCP_Service_2\",\n  \"color\" : \"green\",\n  \"port\" : 5656,\n  \"aggressive-aging\" : {\n    \"default-timeout\" : 3600\n  }\n}",
      "response": "{\n  \"uid\" : \"785a4a8b-8c69-4143-9646-b34ee3b830c5\",\n  \"name\" : \"New_TCP_Service_2\",\n  \"type\" : \"service-tcp\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1479719917748,\n      \"iso-8601\" : \"2016-11-21T11:18+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1479719839437,\n      \"iso-8601\" : \"2016-11-21T11:17+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"light green\",\n  \"icon\" : \"Services/TCPService\",\n  \"groups\" : [ ],\n  \"keep-connections-open-after-policy-installation\" : false,\n  \"session-timeout\" : 0,\n  \"use-default-session-timeout\" : true,\n  \"match-for-any\" : true,\n  \"sync-connections-on-cluster\" : true,\n  \"aggressive-aging\" : {\n    \"enable\" : true,\n    \"timeout\" : 360,\n    \"use-default-timeout\" : false,\n    \"default-timeout\" : 3600\n  },\n  \"port\" : \"5656\",\n  \"match-by-protocol-signature\" : false\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:19.467643",
    "source_file": "set-service-tcp.html"
  }
}
```