# show-threat-rulebase

```json
{
  "command": "show-threat-rulebase",
  "description": "Shows the entire Threat Prevention Rules layer. The reply features a list of rules. Each rule has the Global Exceptions Group attached and may have any number of an Exceptions Group attached. An optional \"filter\" field may be added in order to filter out only those rules that match a search criteria.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-threat-rulebase",
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
        "name": "filter",
        "description": "Search expression to filter the rulebase. The provided text should be exactly the same as it would be given in Smart Console. The logical operators in the expression ('AND', 'OR') should be provided in capital letters. If an operator is not used, the default OR operator applies.",
        "type": "string",
        "required": false
      },
      {
        "name": "filter-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "general",
        "valid_values": [
          "general",
          "packet"
        ]
      },
      {
        "name": "search-mode",
        "description": "When set to 'general', both the Full Text Search and Packet Search are enabled. In this mode, Packet Search will not match on 'Any' object, a negated cell or a group-with-exclusion. When the search-mode is set to 'packet', by default, the match on 'Any' object, a negated cell or a group-with-exclusion are enabled. packet-search-settings may be provided to change the default behavior.",
        "type": "string",
        "required": false,
        "default": "general",
        "valid_values": [
          "general",
          "packet"
        ]
      },
      {
        "name": "packet-search-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "expand-group-members",
        "description": "When true, if the search expression contains a UID or a name of a group object, results will include rules that match on at least one member of the group.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "expand-group-with-exclusion-members",
        "description": "When true, if the search expression contains a UID or a name of a group-with-exclusion object, results will include rules that match at least one member of the \"include\" part and is not a member of the \"except\" part.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "match-on-any",
        "description": "Whether to match on 'Any' object.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "match-on-group-with-exclusion",
        "description": "Whether to match on a group-with-exclusion.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "match-on-negate",
        "description": "Whether to match on a negated cell.",
        "type": "boolean",
        "required": false,
        "default": "true"
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
      },
      {
        "name": "package",
        "description": "Name of the package.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-object-dictionary",
        "description": "N/A",
        "type": "boolean",
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
        "name": "from",
        "description": "From which element number the query was done.",
        "type": "integer",
        "required": false
      },
      {
        "name": "objects-dictionary",
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
        "name": "rulebase",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "type",
        "description": "Rules type.",
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
    "show-threat-rulebase": {
      "description": "Shows the entire Threat Rules Rulebase.",
      "request": "POST {{server}}/show-threat-rulebase\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Threat Prevention\",\n  \"offset\" : 0,\n  \"limit\" : 20,\n  \"details-level\" : \"standard\",\n  \"use-object-dictionary\" : false,\n  \"filter\" : \"\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 3,\n  \"total\" : 3,\n  \"name\" : \"Threat Prevention\",\n  \"uid\" : \"07643e1b-c7fd-4b54-9844-7b8c92135d1e\",\n  \"rulebase\" : [ {\n    \"uid\" : \"e348f8f5-ef7c-4824-9b85-4000ce0df964\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1445233508467,\n        \"iso-8601\" : \"2015-10-19T08:45+0300\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1444909091900,\n        \"iso-8601\" : \"2015-10-15T14:38+0300\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Policy Targets\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n    } ],\n    \"source\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"source-negate\" : false,\n    \"destination\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"destination-negate\" : false,\n    \"service\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"service-negate\" : false,\n    \"protected-scope\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"protected-scope-negate\" : false,\n    \"name\" : \"rule1\",\n    \"track\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Log\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c477\"\n    },\n    \"track-settings\" : {\n      \"packet-capture\" : true\n    },\n    \"action\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiArmadaNewProfile\",\n      \"name\" : \"Recommended_Profile\",\n      \"uid\" : \"44b83c65-e73c-4d63-aa55-4cdcea4a6d4b\"\n    },\n    \"exceptions\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"name\" : \"abc\",\n      \"uid\" : \"54ed2702-9184-477b-ba35-bb162733f3dc\"\n    }, {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"name\" : \"exception1\",\n      \"uid\" : \"f99f6d59-e018-4bd6-be15-e385b549e79e\"\n    }, {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"name\" : \"exception2\",\n      \"uid\" : \"aa42fa65-5eee-4b3d-a532-e1218e5e9326\"\n    } ],\n    \"rule-number\" : 1,\n    \"type\" : \"rule\"\n  }, {\n    \"uid\" : \"e9a60e1f-845f-4f83-a5aa-27eba8a69e22\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1445247340478,\n        \"iso-8601\" : \"2015-10-19T12:35+0300\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1445247318560,\n        \"iso-8601\" : \"2015-10-19T12:35+0300\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Policy Targets\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n    } ],\n    \"source\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"source-negate\" : false,\n    \"destination\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"destination-negate\" : false,\n    \"service\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"service-negate\" : false,\n    \"protected-scope\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"protected-scope-negate\" : false,\n    \"name\" : \"spy\",\n    \"track\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Log\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c477\"\n    },\n    \"track-settings\" : {\n      \"packet-capture\" : true\n    },\n    \"action\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiArmadaNewProfile\",\n      \"name\" : \"Recommended_Profile\",\n      \"uid\" : \"44b83c65-e73c-4d63-aa55-4cdcea4a6d4b\"\n    },\n    \"rule-number\" : 2,\n    \"type\" : \"rule\"\n  }, {\n    \"uid\" : \"570df5aa-427c-4090-896e-dc35b1fdbf42\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1445438243630,\n        \"iso-8601\" : \"2015-10-21T17:37+0300\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1445438243630,\n        \"iso-8601\" : \"2015-10-21T17:37+0300\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Policy Targets\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n    } ],\n    \"source\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"source-negate\" : false,\n    \"destination\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"destination-negate\" : false,\n    \"service\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"service-negate\" : false,\n    \"protected-scope\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"protected-scope-negate\" : false,\n    \"track\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Log\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c477\"\n    },\n    \"track-settings\" : {\n      \"packet-capture\" : true\n    },\n    \"action\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiArmadaNewProfile\",\n      \"name\" : \"Recommended_Profile\",\n      \"uid\" : \"44b83c65-e73c-4d63-aa55-4cdcea4a6d4b\"\n    },\n    \"exceptions\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"uid\" : \"5edf987e-0a83-4fcb-a37f-d71a8e5e9fd5\"\n    }, {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"name\" : \"exception1\",\n      \"uid\" : \"f99f6d59-e018-4bd6-be15-e385b549e79e\"\n    }, {\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"type\" : \"threat-exception\",\n      \"name\" : \"exception2\",\n      \"uid\" : \"aa42fa65-5eee-4b3d-a532-e1218e5e9326\"\n    } ],\n    \"rule-number\" : 3,\n    \"type\" : \"rule\"\n  } ]\n}"
    },
    "show-threat-rulebase-with-filter": {
      "description": "Shows the entire Threat Rules Rulebase.",
      "request": "POST {{server}}/show-threat-rulebase\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Standard Threat Prevention\",\n  \"offset\" : 0,\n  \"limit\" : 20,\n  \"details-level\" : \"standard\",\n  \"use-object-dictionary\" : false,\n  \"filter\" : \"WirelessZone\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 2,\n  \"total\" : 2,\n  \"name\" : \"Standard Threat Prevention\",\n  \"uid\" : \"5244d78e-7749-40e2-8604-4d04bc5ee13f\",\n  \"rulebase\" : [ {\n    \"uid\" : \"25af9a7c-f4e5-4cd5-a6a8-f74f19854db0\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1451453598360,\n        \"iso-8601\" : \"2015-12-30T07:33+0200\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1450930796908,\n        \"iso-8601\" : \"2015-12-24T06:19+0200\"\n      },\n      \"creator\" : \"System\"\n    },\n    \"install-on\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Policy Targets\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n    } ],\n    \"source\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"source-negate\" : false,\n    \"destination\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"destination-negate\" : false,\n    \"service\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"service-negate\" : false,\n    \"protected-scope\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"security-zone\",\n      \"name\" : \"WirelessZone\",\n      \"uid\" : \"57de3848-3675-48ed-b045-41378f4babb3\"\n    } ],\n    \"protected-scope-negate\" : false,\n    \"name\" : \"Rule 1\",\n    \"track\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Log\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c477\"\n    },\n    \"track-settings\" : {\n      \"packet-capture\" : true\n    },\n    \"action\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiArmadaNewProfile\",\n      \"name\" : \"Optimized\",\n      \"uid\" : \"fa1aa324-a8cc-4dbd-bc04-f31fdb8abf61\"\n    },\n    \"rule-number\" : 1,\n    \"type\" : \"rule\"\n  }, {\n    \"uid\" : \"8439c5cd-8879-477c-92af-91ea46b54071\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1451453620395,\n        \"iso-8601\" : \"2015-12-30T07:33+0200\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1451453601902,\n        \"iso-8601\" : \"2015-12-30T07:33+0200\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Policy Targets\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n    } ],\n    \"source\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"source-negate\" : false,\n    \"destination\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"destination-negate\" : false,\n    \"service\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiAnyObject\",\n      \"name\" : \"Any\",\n      \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n    } ],\n    \"service-negate\" : false,\n    \"protected-scope\" : [ {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"security-zone\",\n      \"name\" : \"WirelessZone\",\n      \"uid\" : \"57de3848-3675-48ed-b045-41378f4babb3\"\n    } ],\n    \"protected-scope-negate\" : false,\n    \"name\" : \"Rule 3\",\n    \"track\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"Global\",\n      \"name\" : \"Log\",\n      \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c477\"\n    },\n    \"track-settings\" : {\n      \"packet-capture\" : true\n    },\n    \"action\" : {\n      \"domain\" : {\n        \"domain-type\" : \"data domain\",\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\"\n      },\n      \"type\" : \"CpmiArmadaNewProfile\",\n      \"name\" : \"Optimized\",\n      \"uid\" : \"fa1aa324-a8cc-4dbd-bc04-f31fdb8abf61\"\n    },\n    \"rule-number\" : 2,\n    \"type\" : \"rule\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:29.023393",
    "source_file": "show-threat-rulebase.html"
  }
}
```