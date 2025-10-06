# show-nat-rulebase

```json
{
  "command": "show-nat-rulebase",
  "description": "Shows the entire NAT Rules layer. This layer is divided into sections. A NAT Rule may be within a section, or independent of a section (in which case it is said to be under the \"global\" section). There are two types of sections: auto generated read only sections and general sections which are created manually. The reply features a list of objects. Each object may be a section of the layer, within which its rules may be found, or a rule itself, for the case of rules which are under the global section. An optional \"filter\" field may be added in order to filter out only those rules that match a search criteria.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-nat-rulebase",
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
        "name": "package",
        "description": "Name of the package.",
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
        "name": "show-hits",
        "description": "Show hitcount data.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-object-dictionary",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "hits-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "from-date",
        "description": "Format: YYYY-MM-DD, YYYY-mm-ddThh:mm:ss.",
        "type": "string",
        "required": false
      },
      {
        "name": "target",
        "description": "Target gateway name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-date",
        "description": "Format: YYYY-MM-DD, YYYY-mm-ddThh:mm:ss.",
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
    "show-nat-rulebase": {
      "description": "Shows the entire NAT Rules Rulebase.",
      "request": "POST {{server}}/show-nat-rulebase\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"offset\" : 1,\n  \"limit\" : 2,\n  \"details-level\" : \"standard\",\n  \"use-object-dictionary\" : true,\n  \"package\" : \"standard\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 4,\n  \"total\" : 4,\n  \"uid\" : \"17dd4fab-1940-4760-9a93-9dba4fca9265\",\n  \"rulebase\" : [ {\n    \"uid\" : \"5b149268-1396-4d16-93c9-79d69a49de18\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1445246631813,\n        \"iso-8601\" : \"2015-10-19T12:23+0300\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1445246624363,\n        \"iso-8601\" : \"2015-10-19T12:23+0300\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ \"6c488338-8eec-4103-ad21-cd461ac2c476\" ],\n    \"auto-generated\" : false,\n    \"original-destination\" : \"57de3848-3675-48ed-b045-41378f4babb3\",\n    \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"original-source\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n    \"translated-source\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"original-service\" : \"97aeb44f-9aea-11d5-bd16-0090272ccb30\",\n    \"translated-service\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"method\" : \"static\",\n    \"rule-number\" : 1,\n    \"type\" : \"rule\"\n  }, {\n    \"uid\" : \"c35c7d9f-0730-437a-af0e-ec161284f2e8\",\n    \"enabled\" : true,\n    \"comments\" : \"\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"read-only\" : false,\n      \"last-modify-time\" : {\n        \"posix\" : 1445246621205,\n        \"iso-8601\" : \"2015-10-19T12:23+0300\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1445246609436,\n        \"iso-8601\" : \"2015-10-19T12:23+0300\"\n      },\n      \"creator\" : \"aa\"\n    },\n    \"install-on\" : [ \"6c488338-8eec-4103-ad21-cd461ac2c476\" ],\n    \"auto-generated\" : false,\n    \"original-destination\" : \"8a883654-cdd4-45a8-b079-d4e476a70ad6\",\n    \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"original-source\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n    \"translated-source\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"original-service\" : \"97aeb3d6-9aea-11d5-bd16-0090272ccb30\",\n    \"translated-service\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n    \"method\" : \"static\",\n    \"rule-number\" : 2,\n    \"type\" : \"rule\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Automatic Generated Rules : Machine Static NAT\",\n    \"uid\" : \"785f43ba-efb5-43bb-b196-4e539bb4d014\",\n    \"type\" : \"section\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Automatic Generated Rules : Machine Hide NAT\",\n    \"uid\" : \"50755a21-ca90-4a26-a285-21179e233e7b\",\n    \"type\" : \"section\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Automatic Generated Rules : Address Range Static NAT\",\n    \"uid\" : \"22d6b639-ce3b-4d20-b1a7-d96ac6df5d6d\",\n    \"type\" : \"section\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Automatic Generated Rules : Network Static NAT\",\n    \"uid\" : \"232ec587-cd3f-454e-a400-26a7fa16233c\",\n    \"type\" : \"section\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Automatic Generated Rules : Address Range Hide NAT\",\n    \"uid\" : \"d6379e8a-ee2b-48f6-8096-e5d58443829e\",\n    \"type\" : \"section\"\n  }, {\n    \"from\" : 3,\n    \"to\" : 4,\n    \"rulebase\" : [ {\n      \"uid\" : \"f49dcfe4-3788-450f-91a0-c884a75c51df\",\n      \"enabled\" : true,\n      \"comments\" : \"\",\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"read-only\" : false,\n        \"last-modify-time\" : {\n          \"posix\" : 1444712139520,\n          \"iso-8601\" : \"2015-10-13T07:55+0300\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1444712139520,\n          \"iso-8601\" : \"2015-10-13T07:55+0300\"\n        },\n        \"creator\" : \"System\"\n      },\n      \"install-on\" : [ \"97aeb368-9aea-11d5-bd16-0090272ccb30\" ],\n      \"auto-generated\" : true,\n      \"original-destination\" : \"7559e93f-a5d1-4d77-991e-33e99ce2db71\",\n      \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-source\" : \"7559e93f-a5d1-4d77-991e-33e99ce2db71\",\n      \"translated-source\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-service\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-service\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"method\" : \"hide\",\n      \"rule-number\" : 3,\n      \"type\" : \"rule\"\n    }, {\n      \"uid\" : \"5ba26dc2-dded-4c5f-8c73-7b1b0d5c7922\",\n      \"enabled\" : true,\n      \"comments\" : \"\",\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"read-only\" : false,\n        \"last-modify-time\" : {\n          \"posix\" : 1444712139533,\n          \"iso-8601\" : \"2015-10-13T07:55+0300\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1444712139533,\n          \"iso-8601\" : \"2015-10-13T07:55+0300\"\n        },\n        \"creator\" : \"System\"\n      },\n      \"install-on\" : [ \"97aeb368-9aea-11d5-bd16-0090272ccb30\" ],\n      \"auto-generated\" : true,\n      \"original-destination\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-source\" : \"7559e93f-a5d1-4d77-991e-33e99ce2db71\",\n      \"translated-source\" : \"7559e93f-a5d1-4d77-991e-33e99ce2db71\",\n      \"original-service\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-service\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"method\" : \"hide\",\n      \"rule-number\" : 4,\n      \"type\" : \"rule\"\n    } ],\n    \"name\" : \"Automatic Generated Rules : Network Hide NAT\",\n    \"uid\" : \"3c7d9a48-0b52-4325-b073-dbce47839f64\",\n    \"type\" : \"section\"\n  }, {\n    \"rulebase\" : [ ],\n    \"name\" : \"Manual Lower Rules\",\n    \"uid\" : \"9ddb00ec-b9c7-481d-af85-d435eaba1947\",\n    \"type\" : \"section\"\n  } ],\n  \"objects-dictionary\" : [ {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"service-tcp\",\n    \"name\" : \"AOL\",\n    \"uid\" : \"97aeb44f-9aea-11d5-bd16-0090272ccb30\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"CpmiAnyObject\",\n    \"name\" : \"All\",\n    \"uid\" : \"97aeb368-9aea-11d5-bd16-0090272ccb30\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"CpmiAnyObject\",\n    \"name\" : \"Any\",\n    \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"network\",\n    \"name\" : \"CP_default_Office_Mode_addresses_pool\",\n    \"uid\" : \"7559e93f-a5d1-4d77-991e-33e99ce2db71\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"dynamic-object\",\n    \"name\" : \"DMZNet\",\n    \"uid\" : \"8a883654-cdd4-45a8-b079-d4e476a70ad6\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"Global\",\n    \"name\" : \"Original\",\n    \"uid\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"Global\",\n    \"name\" : \"Policy Targets\",\n    \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"security-zone\",\n    \"name\" : \"WirelessZone\",\n    \"uid\" : \"57de3848-3675-48ed-b045-41378f4babb3\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"service-udp\",\n    \"name\" : \"archie\",\n    \"uid\" : \"97aeb3d6-9aea-11d5-bd16-0090272ccb30\"\n  } ]\n}"
    },
    "show-nat-rulebase-with-filter": {
      "description": "Shows the entire NAT Rules Rulebase.",
      "request": "POST {{server}}/show-nat-rulebase\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"offset\" : 0,\n  \"limit\" : 50,\n  \"details-level\" : \"standard\",\n  \"use-object-dictionary\" : true,\n  \"package\" : \"standard\",\n  \"filter\" : \"ssh_version_2\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 2,\n  \"total\" : 2,\n  \"uid\" : \"4862b29a-1753-4d19-9142-6814c7377474\",\n  \"rulebase\" : [ {\n    \"from\" : 1,\n    \"to\" : 2,\n    \"rulebase\" : [ {\n      \"uid\" : \"86fc210c-9fa4-4cfa-83bb-d6377853dd20\",\n      \"enabled\" : true,\n      \"comments\" : \"rule for RND members  RNDNetwork-> RND to Internal Network\",\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"read-only\" : false,\n        \"last-modify-time\" : {\n          \"posix\" : 1450932209522,\n          \"iso-8601\" : \"2015-12-24T06:43+0200\"\n        },\n        \"last-modifier\" : \"aa\",\n        \"creation-time\" : {\n          \"posix\" : 1450932130503,\n          \"iso-8601\" : \"2015-12-24T06:42+0200\"\n        },\n        \"creator\" : \"aa\"\n      },\n      \"install-on\" : [ \"6c488338-8eec-4103-ad21-cd461ac2c476\" ],\n      \"auto-generated\" : false,\n      \"original-destination\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-source\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-source\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-service\" : \"cd082d9a-44a6-4cef-a17d-5541029adfb3\",\n      \"translated-service\" : \"cd082d9a-44a6-4cef-a17d-5541029adfb3\",\n      \"method\" : \"static\",\n      \"rule-number\" : 1,\n      \"type\" : \"rule\"\n    }, {\n      \"uid\" : \"e47a64af-8af0-4a2f-8f54-5fbdcdc252a5\",\n      \"enabled\" : true,\n      \"comments\" : \"\",\n      \"domain\" : {\n        \"domain-type\" : \"domain\",\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"read-only\" : false,\n        \"last-modify-time\" : {\n          \"posix\" : 1451453576971,\n          \"iso-8601\" : \"2015-12-30T07:32+0200\"\n        },\n        \"last-modifier\" : \"aa\",\n        \"creation-time\" : {\n          \"posix\" : 1451453557603,\n          \"iso-8601\" : \"2015-12-30T07:32+0200\"\n        },\n        \"creator\" : \"aa\"\n      },\n      \"install-on\" : [ \"6c488338-8eec-4103-ad21-cd461ac2c476\" ],\n      \"auto-generated\" : false,\n      \"original-destination\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-destination\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-source\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n      \"translated-source\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"original-service\" : \"cd082d9a-44a6-4cef-a17d-5541029adfb3\",\n      \"translated-service\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\",\n      \"method\" : \"static\",\n      \"rule-number\" : 2,\n      \"type\" : \"rule\"\n    } ],\n    \"name\" : \"Manual Lower Rules\",\n    \"uid\" : \"b65894d2-b2ce-435b-ab31-17678c3fee4e\",\n    \"type\" : \"section\"\n  } ],\n  \"objects-dictionary\" : [ {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"CpmiAnyObject\",\n    \"name\" : \"Any\",\n    \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"Global\",\n    \"name\" : \"Original\",\n    \"uid\" : \"85c0f50f-6d8a-4528-88ab-5fb11d8fe16c\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"Global\",\n    \"name\" : \"Policy Targets\",\n    \"uid\" : \"6c488338-8eec-4103-ad21-cd461ac2c476\"\n  }, {\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"service-tcp\",\n    \"name\" : \"ssh_version_2\",\n    \"uid\" : \"cd082d9a-44a6-4cef-a17d-5541029adfb3\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:26.379126",
    "source_file": "show-nat-rulebase.html"
  }
}
```