# add-idp-administrator-group

```json
{
  "command": "add-idp-administrator-group",
  "description": "Create new Identity Provider administrators group.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-idp-administrator-group",
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
        "name": "group-id",
        "description": "Group ID or Name should be set base on the source attribute of 'groups' in the Saml Assertion.",
        "type": "string",
        "required": true
      },
      {
        "name": "multi-domain-profile",
        "description": "Administrator multi-domain profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "permissions-profile",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "domain",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "profile",
        "description": "Permission profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "domain",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "profile",
        "description": "Permission profile.",
        "type": "string",
        "required": false
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
        "name": "group-id",
        "description": "Group ID or Name should be set base on the source attribute of 'groups' in the Saml Assertion.",
        "type": "string",
        "required": false
      },
      {
        "name": "multi-domain-profile",
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
        "name": "permissions-profile",
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
    "add group with domain super user profile": {
      "description": "add group with domain super user profile",
      "request": "POST {{server}}/add-idp-administrator-group\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my super group\",\n  \"group-id\" : \"it-team\",\n  \"multi-domain-profile\" : \"domain super user\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": "{\n  \"uid\" : \"799fba94-d915-46d0-82a6-6e6bf369e87c\",\n  \"name\" : \"my super group\",\n  \"type\" : \"idp-administrator-group\",\n  \"domain\" : {\n    \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n    \"name\" : \"System Data\",\n    \"domain-type\" : \"mds\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1637845907740,\n      \"iso-8601\" : \"2021-11-25T15:11+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1637845907740,\n      \"iso-8601\" : \"2021-11-25T15:11+0200\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"General/AdministratorGroup\",\n  \"multi-domain-profile\" : {\n    \"uid\" : \"fc548fad-48ab-4bbe-b693-00105d536006\",\n    \"name\" : \"Domain Super User\",\n    \"type\" : \"MDPermissionRole\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"General/Role\",\n    \"color\" : \"black\"\n  },\n  \"group-id\" : \"it-team\"\n}"
    },
    "add group with global manager profile": {
      "description": "add group with global manager profile",
      "request": "POST {{server}}/add-idp-administrator-group\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my global group2\",\n  \"group-id\" : \"global-team1\",\n  \"multi-domain-profile\" : \"global manager\",\n  \"permissions-profile\" : [ {\n    \"domain\" : \"DomA\",\n    \"profile\" : \"read only all\"\n  }, {\n    \"domain\" : \"All Global Domains\",\n    \"profile\" : \"read write all\"\n  } ]\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": "{\n  \"uid\" : \"f5fa4f14-c2b3-490c-bb09-73f03c19e75e\",\n  \"name\" : \"my global group2\",\n  \"type\" : \"idp-administrator-group\",\n  \"domain\" : {\n    \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n    \"name\" : \"System Data\",\n    \"domain-type\" : \"mds\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1637847695133,\n      \"iso-8601\" : \"2021-11-25T15:41+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1637847695133,\n      \"iso-8601\" : \"2021-11-25T15:41+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"General/AdministratorGroup\",\n  \"multi-domain-profile\" : {\n    \"uid\" : \"6f2d198b-0ca5-480b-88f2-30217da0d635\",\n    \"name\" : \"Global Manager\",\n    \"type\" : \"MDPermissionRole\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"General/Role\",\n    \"color\" : \"black\"\n  },\n  \"permissions-profile\" : [ {\n    \"domain\" : {\n      \"uid\" : \"68efd634-fd04-481b-b62d-99a2a2a6a7d4\",\n      \"name\" : \"All Global Domains\",\n      \"type\" : \"Folder\",\n      \"domain\" : {\n        \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n        \"name\" : \"System Data\",\n        \"domain-type\" : \"mds\"\n      },\n      \"icon\" : \"Objects/allGlobalDomains\",\n      \"color\" : \"black\"\n    },\n    \"profile\" : {\n      \"uid\" : \"3c8bf435-6bdc-4dec-aab0-5af53bbf946b\",\n      \"name\" : \"Read Write All\",\n      \"type\" : \"PermissionRole\",\n      \"domain\" : {\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\",\n        \"domain-type\" : \"data domain\"\n      },\n      \"icon\" : \"General/Role\",\n      \"color\" : \"black\"\n    }\n  }, {\n    \"domain\" : {\n      \"uid\" : \"18b7fdfa-4fa5-490a-b862-2add6b2ed375\",\n      \"name\" : \"DomA\",\n      \"type\" : \"FolderMirror\",\n      \"domain\" : {\n        \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n        \"name\" : \"System Data\",\n        \"domain-type\" : \"mds\"\n      },\n      \"icon\" : \"General/globalsNa\",\n      \"color\" : \"black\"\n    },\n    \"profile\" : {\n      \"uid\" : \"f4a23218-5bb9-4880-94bb-9c06b951f195\",\n      \"name\" : \"Read Only All\",\n      \"type\" : \"PermissionRole\",\n      \"domain\" : {\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\",\n        \"domain-type\" : \"data domain\"\n      },\n      \"icon\" : \"General/Role\",\n      \"color\" : \"black\"\n    }\n  } ],\n  \"group-id\" : \"global-team1\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:07.457587",
    "source_file": "add-idp-administrator-group.html"
  }
}
```