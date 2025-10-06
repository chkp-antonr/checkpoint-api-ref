# add-network

```json
{
  "command": "add-network",
  "description": "Create new object.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-network",
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
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "subnet",
        "description": "IPv4 or IPv6 network address. If both addresses are required use subnet4 and subnet6 fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "mask-length",
        "description": "IPv4 or IPv6 network mask length. If both masks are required use mask-length4 and mask-length6 fields explicitly. Instead of IPv4 mask length it is possible to specify IPv4 mask itself in subnet-mask field.",
        "type": "integer",
        "required": true
      },
      {
        "name": "nat-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "auto-rule",
        "description": "Whether to add automatic address translation rules.",
        "type": "boolean",
        "required": true,
        "default": "false"
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly. This parameter is not required in case \"method\" parameter is \"hide\" and \"hide-behind\" parameter is \"gateway\".",
        "type": "string",
        "required": true
      },
      {
        "name": "hide-behind",
        "description": "Hide behind method. This parameter is forbidden in case \"method\" parameter is \"static\".",
        "type": "string",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "install-on",
        "description": "Which gateway should apply the NAT translation.",
        "type": "string",
        "required": false
      },
      {
        "name": "method",
        "description": "NAT translation method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hide",
          "static"
        ]
      },
      {
        "name": "broadcast",
        "description": "Allow broadcast address inclusion.",
        "type": "string",
        "required": false,
        "valid_values": [
          "disallow",
          "allow"
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
        "name": "subnet4",
        "description": "IPv4 network address.",
        "type": "string",
        "required": false
      },
      {
        "name": "subnet6",
        "description": "IPv6 network address.",
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
        "name": "broadcast",
        "description": "Allow broadcast address inclusion.",
        "type": "string",
        "required": false,
        "valid_values": [
          "disallow",
          "allow"
        ]
      },
      {
        "name": "mask-length4",
        "description": "IPv4 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "mask-length6",
        "description": "IPv6 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "subnet-mask",
        "description": "IPv4 network mask.",
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
        "name": "nat-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "auto-rule",
        "description": "Whether to add automatic address translation rules.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "hide-behind",
        "description": "Hide behind method. This parameter is forbidden in case \"method\" parameter is \"static\".",
        "type": "string",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "install-on",
        "description": "Which gateway should apply the NAT translation.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "method",
        "description": "NAT translation method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hide",
          "static"
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
    "add-network": {
      "description": "",
      "request": "POST {{server}}/add-network\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"New Network 1\",\n  \"subnet\" : \"192.0.2.0\",\n  \"subnet-mask\" : \"255.255.255.0\"\n}",
      "response": ""
    },
    "add-network-with-NAT-static": {
      "description": "",
      "request": "POST {{server}}/add-network\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"New Network 3\",\n  \"subnet\" : \"192.0.2.0\",\n  \"subnet-mask\" : \"255.255.255.0\",\n  \"nat-settings\" : {\n    \"auto-rule\" : true,\n    \"method\" : \"static\",\n    \"ip-address\" : \"192.0.2.1\",\n    \"install-on\" : \"All\"\n  }\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:08.138705",
    "source_file": "add-network.html"
  }
}
```