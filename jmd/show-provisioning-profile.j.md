# show-provisioning-profile

```json
{
  "command": "show-provisioning-profile",
  "description": "Retrieve existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-provisioning-profile",
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
        "name": "configuration-script",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "configuration-script-base64",
        "description": "Configuration script in base64.",
        "type": "string",
        "required": false
      },
      {
        "name": "dns",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "dns-proxy",
        "description": "DNS proxy enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "primary-server",
        "description": "Primary DNS Server.",
        "type": "string",
        "required": false
      },
      {
        "name": "secondary-server",
        "description": "Secondary DNS Server.",
        "type": "string",
        "required": false
      },
      {
        "name": "servers-configuration-mode",
        "description": "Servers configuration mode. Auto- dns configuration provided by the active internet connection. Manual- set dns servers configuration manually.",
        "type": "string",
        "required": false
      },
      {
        "name": "tertiary-server",
        "description": "Tertiary DNS Server.",
        "type": "string",
        "required": false
      },
      {
        "name": "domain-name",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "name",
        "description": "Domain Name.",
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
        "name": "hosts",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "hosts",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "host-ip-address",
        "description": "Host IP-Address.",
        "type": "string",
        "required": false
      },
      {
        "name": "host-name",
        "description": "Host Name.",
        "type": "string",
        "required": false
      },
      {
        "name": "hotspot",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "enabled",
        "description": "Hotspot enabled on device.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "portal-title",
        "description": "Portal title.",
        "type": "string",
        "required": false
      },
      {
        "name": "portal-message",
        "description": "Portal message.",
        "type": "string",
        "required": false
      },
      {
        "name": "display-terms-of-use",
        "description": "Use terms of use.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "terms-of-use",
        "description": "Terms of use.",
        "type": "string",
        "required": false
      },
      {
        "name": "require-authentication",
        "description": "Require authentication.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allow-users-from-specific-group",
        "description": "Allow users from specific group.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allowed-users-groups",
        "description": "Allowed users groups.",
        "type": "array",
        "required": false
      },
      {
        "name": "radius",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "manage-settings",
        "description": "Manage settings mode: locally on the device or centrally from this application.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-settings",
        "description": "Override settings mode: allowed, mandatory or denied. Relevant only when settings are managed centrally.",
        "type": "string",
        "required": false
      },
      {
        "name": "enabled",
        "description": "RADIUS enabled on device.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "radius-servers",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "radius-server-name",
        "description": "Radius server Name.",
        "type": "string",
        "required": false
      },
      {
        "name": "allow-administrators-from-specific-radius-group-only",
        "description": "Allow administrators from specific radius group only.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allowed-radius-groups",
        "description": "Allowed radius groups.",
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
    "show-provisioning-profile": {
      "description": "",
      "request": "POST {{server}}/show-provisioning-profile\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"prv_gaia_profile\"\n}",
      "response": "{\n  \"uid\" : \"ea51c98a-65aa-3f43-bca8-582c379226c8\",\n  \"name\" : \"SMBCluster\",\n  \"type\" : \"provisioning-profile\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"dns\" : {\n    \"primary-server\" : \"194.29.40.221\",\n    \"secondary-server\" : \"194.29.40.220\",\n    \"tertiary-server\" : \"\",\n    \"dns-proxy\" : true,\n    \"servers-configuration-mode\" : \"manual\",\n    \"manage-settings\" : \"locally on the device\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"hosts\" : {\n    \"manage-settings\" : \"centrally from this application\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"domain-name\" : {\n    \"manage-settings\" : \"centrally from this application\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"radius\" : {\n    \"enabled\" : false,\n    \"allow-administrators-from-specific-radius-group-only\" : false,\n    \"manage-settings\" : \"centrally from this application\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"hotspot\" : {\n    \"enabled\" : false,\n    \"display-terms-of-use\" : false,\n    \"require-authentication\" : false,\n    \"allow-users-from-specific-group\" : false,\n    \"manage-settings\" : \"centrally from this application\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"configuration-script\" : {\n    \"manage-settings\" : \"centrally from this application\",\n    \"override-settings\" : \"allowed\"\n  },\n  \"groups\" : [ {\n    \"uid\" : \"a5a615ca-ed33-e045-970e-4511a931a215\",\n    \"name\" : \"C_SMB_68_34\",\n    \"type\" : \"\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"Unknown\"\n  }, {\n    \"uid\" : \"615f88ce-5962-8146-9d60-e2b9647ff974\",\n    \"name\" : \"C_SMB_68_29\",\n    \"type\" : \"\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"Unknown\"\n  } ],\n  \"comments\" : \"\",\n  \"icon\" : \"NetworkObjects/ROBO/Profile_Provisioning\",\n  \"tags\" : [ ],\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1629971663134,\n      \"iso-8601\" : \"2021-08-26T12:54+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1629800112921,\n      \"iso-8601\" : \"2021-08-24T13:15+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"read-only\" : false\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:26.842305",
    "source_file": "show-provisioning-profile.html"
  }
}
```