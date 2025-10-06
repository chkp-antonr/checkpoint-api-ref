# show-services-dce-rpc

```json
{
  "command": "show-services-dce-rpc",
  "description": "Retrieve all objects.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-services-dce-rpc",
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
    "show-services-dce-rpc": {
      "description": "",
      "request": "POST {{server}}/show-services-dce-rpc\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"limit\" : 50,\n  \"offset\" : 0,\n  \"details-level\" : \"standard\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 42,\n  \"total\" : 42,\n  \"objects\" : [ {\n    \"uid\" : \"3d0d46b6-4ddb-43e0-9faa-c969dbc3e19f\",\n    \"name\" : \"ALL_DCE_RPC\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"f11e31f1-0127-1e46-a838-4401232ee78b\",\n    \"name\" : \"DCOM-IRemUnknown\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"0e61be34-2b17-894d-b155-471b2119c309\",\n    \"name\" : \"DCOM-IWbemLevel1Login\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"024291a5-bc3e-4c96-8d82-513f3336a9f6\",\n    \"name\" : \"DCOM-OXID_Resolver\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"4e68ca9c-c624-47a5-b2bc-02f1197c8e35\",\n    \"name\" : \"DCOM-RemUnknown2\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"5c66b970-e289-4b39-89ea-4f0f19a389d7\",\n    \"name\" : \"DCOM-RemoteActivation\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"38910079-ea24-4df6-bd98-d1c67f90df4a\",\n    \"name\" : \"DCOM-SystemActivation\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"ed771ab7-acd8-4a40-ba23-de37f1275d0c\",\n    \"name\" : \"EndPointMapper\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb464-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCctla\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb466-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCctla-bulk\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb465-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCctla-cfgpush\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb460-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCdistm\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb463-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCmsgrd-coa\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb462-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCmsgrd-m2m\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb461-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"HP-OpCmsgrd-std\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"617c3a2c-41ac-6a4a-8272-8f00ec5258dd\",\n    \"name\" : \"IWbemFetchSmartEnum\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"363b46f7-3291-6d4e-b8c9-11c17e19827a\",\n    \"name\" : \"IWbemServices\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"7591fc8a-1e03-ae40-819b-cec6a659c066\",\n    \"name\" : \"IWbemWCOSmartEnum\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"73ee702f-46bc-7842-ab62-4914930fadfd\",\n    \"name\" : \"IenumWbemClassObject\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb457-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeADL\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb452-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeDSNSPI\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb453-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeDSRep\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb454-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeDSXDS\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"e4253ee5-95c8-1742-b4fe-550f6ff43e70\",\n    \"name\" : \"MSExchangeDatabase\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"01693eed-3f81-44d3-b498-51696722cc32\",\n    \"name\" : \"MSExchangeDirRef\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb458-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeDirRep\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb455-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeIS\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"592a5d9e-06be-d241-953f-b2663f30ffc9\",\n    \"name\" : \"MSExchangeIS_Async\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"9a4425f1-2cd2-984d-9760-6b1383beaeaa\",\n    \"name\" : \"MSExchangeInformationStore1\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"0215f412-d0c9-6541-a83a-07b99b993b0c\",\n    \"name\" : \"MSExchangeInformationStore2\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"712eb227-3e98-f240-a937-a817eba9e4d2\",\n    \"name\" : \"MSExchangeInformationStore3\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb456-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeMTA\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"d4ae57d8-83c8-9a45-a3a1-a18ee4fd75d2\",\n    \"name\" : \"MSExchangeQAdmin\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"e7885981-2de7-4044-ad4f-d146825edd80\",\n    \"name\" : \"MSExchangeSTOREAsyncEMSMDB\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb45b-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeStoreAdm\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"01cbe864-8881-564d-8b85-17cda468ba4e\",\n    \"name\" : \"MSExchangeStoreAdmin1\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"ad267c2c-8b26-9c40-92d9-4f46c47d1b5c\",\n    \"name\" : \"MSExchangeStoreAdmin3\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb459-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeSysAtt\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"97aeb45a-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"MSExchangeSysAttPriv\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    }\n  }, {\n    \"uid\" : \"e736a918-a7be-fb4e-80bf-066daebec607\",\n    \"name\" : \"MSMQ\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  }, {\n    \"uid\" : \"7d19e3dd-8da5-48a1-b0e0-533fcc0b8dfe\",\n    \"name\" : \"New_DCE-RPC_Service_2\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    }\n  }, {\n    \"uid\" : \"d7d41198-4aa4-d044-a756-434e9694723b\",\n    \"name\" : \"RPCManagement\",\n    \"type\" : \"service-dce-rpc\",\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-cebcebcebceb\",\n      \"name\" : \"IPS Data\"\n    }\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:27.668406",
    "source_file": "show-services-dce-rpc.html"
  }
}
```