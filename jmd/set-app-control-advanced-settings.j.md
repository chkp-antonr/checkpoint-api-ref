# set-app-control-advanced-settings

```json
{
  "command": "set-app-control-advanced-settings",
  "description": "Edit Application Control & URL Filtering Blades' Settings.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-app-control-advanced-settings",
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
        "name": "internal-error-fail-mode",
        "description": "In case of internal system error, allow or block all connections.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow connections",
          "block connections"
        ]
      },
      {
        "name": "url-filtering-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "categorize-https-websites",
        "description": "This option lets Application and URL Filtering assign categories to HTTPS sites without activating HTTPS inspection. It assigns a site category based on its domain name and whether the site has a valid certificate. If the server certificate is: Trusted - Application and URL Filtering gets the domain name from the certificate and uses it to categorize the site.Not Trusted - Application and URL Filtering assigns a category based on the IP address.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enforce-safe-search",
        "description": "Select this option to require use of the safe search feature in search engines. When activated, the URL Filtering Policy uses the strictest available safe search option for the specified search engine.This option overrides user specified search engine options to block offensive material in search results.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "categorize-cached-and-translated-pages",
        "description": "Select this option to assign categories to cached search engine results and translated pages.When this option is selected, Application and URL Filtering assigns categories based on the original Web site instead of the 'search engine pages' category.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-browsing-services",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "Adds to collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "match-application-on-any-port",
        "description": "Match Web application on 'Any' port when used in Block rule - By default this is set to true. and so applications are matched on all services when used in a Block rule.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-web-browsing",
        "description": "If you do not enable URL Filtering on the Security Gateway, you can use a generic Web browser application called Web Browsing in the rule.This application includes all HTTP traffic that is not a defined application Application and URL Filtering assigns Web Browsing as the default application for all HTTP traffic that does not match an application in the Application and URL Filtering Database.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "httpi-non-standard-ports",
        "description": "Enable HTTP inspection on non standard ports for application and URL filtering.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "block-request-when-web-service-is-unavailable",
        "description": "Block requests when the web service is unavailable. When selected, requests are blocked when there is no connectivity to the Check Point Online Web Service.When cleared, requests are allowed when there is no connectivity.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "website-categorization-mode",
        "description": "Hold - Requests are blocked until categorization is complete.Background - Requests are allowed until categorization is complete.Custom - configure different settings depending on the service -Lets you set different modes for URL Filtering and Social Networking Widgets.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "custom-categorization-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "url-filtering-mode",
        "description": "Hold - Requests are blocked until categorization is complete.Background - Requests are allowed until categorization is complete.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "social-network-widgets-mode",
        "description": "Hold - Requests are blocked until categorization is complete.Background - Requests are allowed until categorization is complete.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "categorize-social-network-widgets",
        "description": "When selected, the Security Gateway connects to the Check Point Online Web Service to identify social networking widgets that it does not recognize.When cleared or there is no connectivity between the Security Gateway and the Check Point Online Web, the unknown widget is treated as Web Browsing traffic.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "domain-level-permission",
        "description": "Allows the editing of applications, categories, and services. This property is used only in the Global Domain of an MDS machine.",
        "type": "boolean",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
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
        "name": "internal-error-fail-mode",
        "description": "In case of internal system error, allow or block all connections.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow connections",
          "block connections"
        ]
      },
      {
        "name": "url-filtering-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "categorize-https-websites",
        "description": "This option lets Application and URL Filtering assign categories to HTTPS sites without activating HTTPS inspection. It assigns a site category based on its domain name and whether the site has a valid certificate. If the server certificate is: Trusted - Application and URL Filtering gets the domain name from the certificate and uses it to categorize the site.Not Trusted - Application and URL Filtering assigns a category based on the IP address.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enforce-safe-search",
        "description": "Select this option to require use of the safe search feature in search engines. When activated, the URL Filtering Policy uses the strictest available safe search option for the specified search engine.This option overrides user specified search engine options to block offensive material in search results.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "categorize-cached-and-translated-pages",
        "description": "Select this option to assign categories to cached search engine results and translated pages.When this option is selected, Application and URL Filtering assigns categories based on the original Web site instead of the 'search engine pages' category.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-browsing-services",
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
        "name": "match-application-on-any-port",
        "description": "Match Web application on 'Any' port when used in Block rule - By default this is set to true. and so applications are matched on all services when used in a Block rule.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-web-browsing",
        "description": "If you do not enable URL Filtering on the Security Gateway, you can use a generic Web browser application called Web Browsing in the rule.This application includes all HTTP traffic that is not a defined application Application and URL Filtering assigns Web Browsing as the default application for all HTTP traffic that does not match an application in the Application and URL Filtering Database.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "httpi-non-standard-ports",
        "description": "Enable HTTP inspection on non standard ports for application and URL filtering.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "block-request-when-web-service-is-unavailable",
        "description": "Block requests when the web service is unavailable. When selected, requests are blocked when there is no connectivity to the Check Point Online Web Service.When cleared, requests are allowed when there is no connectivity.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "website-categorization-mode",
        "description": "This option lets Application and URL Filtering assign categories to HTTPS sites without activating HTTPS inspection. It assigns a site category based on its domain name and whether the site has a valid certificate. If the server certificate is: Trusted - Application and URL Filtering gets the domain name from the certificate and uses it to categorize the site.Not Trusted - Application and URL Filtering assigns a category based on the IP address.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "custom-categorization-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "url-filtering-mode",
        "description": "Hold - Requests are blocked until categorization is complete.Background - Requests are allowed until categorization is complete.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "social-network-widgets-mode",
        "description": "Hold - Requests are blocked until categorization is complete.Background - Requests are allowed until categorization is complete.This property is not available in the Global domain of an MDS machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "categorize-social-network-widgets",
        "description": "When selected, the Security Gateway connects to the Check Point Online Web Service to identify social networking widgets that it does not recognize.When cleared or there is no connectivity between the Security Gateway and the Check Point Online Web, the unknown widget is treated as Web Browsing traffic.This property is not available in the Global domain of an MDS machine.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "domain-level-permission",
        "description": "Allows the editing of applications, categories, and services. This property is used only in the Global Domain of an MDS machine.",
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
    "set-app-control-advanced-settings": {
      "description": "",
      "request": "POST {{server}}/set-app-control-advanced-settings\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"internal-error-fail-mode\" : \"block connections\",\n  \"url-filtering-settings.categorize-https-websites\" : \"true\",\n  \"url-filtering-settings.enforce-safe-search\" : \"true\",\n  \"url-filtering-settings.categorize-cached-and-translated-pages\" : \"false\",\n  \"web-browsing-services.add.1\" : \"AH\",\n  \"match-application-on-any-port\" : \"true\",\n  \"enable-web-browsing\" : \"true\",\n  \"httpi-non-standard-ports\" : \"true\",\n  \"block-request-when-web-service-is-unavailable\" : \"true\",\n  \"website-categorization-mode\" : \"custom\",\n  \"custom-categorization-settings.url-filtering-mode\" : \"hold\",\n  \"custom-categorization-settings.social-network-widgets-mode\" : \"background\",\n  \"categorize-social-network-widgets\" : \"true\"\n}",
      "response": "{\n  \"uid\" : \"0d9fcf03-ba25-4ee3-9080-f555f91b5716\",\n  \"type\" : \"app-control-advanced-settings\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1678712561818,\n      \"iso-8601\" : \"2023-03-13T15:02+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1675750866427,\n      \"iso-8601\" : \"2023-02-07T08:21+0200\"\n    },\n    \"creator\" : \"System\"\n  },\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"true\"\n  },\n  \"read-only\" : false,\n  \"internal-error-fail-mode\" : \"block connections\",\n  \"url-filtering-settings\" : {\n    \"categorize-https-websites\" : true,\n    \"enforce-safe-search\" : true,\n    \"categorize-cached-and-translated-pages\" : false\n  },\n  \"session-unification-timeout\" : 180,\n  \"web-browsing-services\" : [ {\n    \"uid\" : \"97aeb3d0-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"ftp\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/FTP\",\n    \"color\" : \"forest green\",\n    \"port\" : \"21\"\n  }, {\n    \"uid\" : \"97aeb3d4-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"http\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"forest green\",\n    \"port\" : \"80\"\n  }, {\n    \"uid\" : \"2a2ca572-fbe7-4e7f-92e4-164f5b4fded1\",\n    \"name\" : \"HTTP_and_HTTPS_proxy\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Services/TCPService\",\n    \"color\" : \"black\",\n    \"port\" : \"8080\"\n  }, {\n    \"uid\" : \"97aeb443-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"https\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"red\",\n    \"port\" : \"443\"\n  }, {\n    \"uid\" : \"8eddeaa0-259d-448f-95b6-490a39f55962\",\n    \"name\" : \"HTTP_proxy\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"orange\",\n    \"port\" : \"8080\"\n  }, {\n    \"uid\" : \"97aeb422-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"AH\",\n    \"type\" : \"service-other\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Services/OtherService\",\n    \"color\" : \"cyan\"\n  } ],\n  \"match-application-on-any-port\" : true,\n  \"enable-web-browsing\" : true,\n  \"httpi-non-standard-ports\" : true,\n  \"unify-connections\" : false,\n  \"issue-separate-log-per-domain\" : true,\n  \"block-request-when-web-service-is-unavailable\" : true,\n  \"website-categorization-mode\" : \"custom\",\n  \"custom-categorization-settings\" : {\n    \"url-filtering-mode\" : \"hold\",\n    \"social-network-widgets-mode\" : \"background\"\n  },\n  \"categorize-social-network-widgets\" : true\n}"
    },
    "set-app-control-advanced-settings in Global domain": {
      "description": "",
      "request": "POST {{server}}/set-app-control-advanced-settings\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"web-browsing-services.add.1\" : \"AH\",\n  \"match-application-on-any-port\" : \"true\",\n  \"domain-level-permission\" : \"false\"\n}",
      "response": "{\n  \"uid\" : \"4d009bbb-287b-4691-a04b-d027abd7793a\",\n  \"type\" : \"app-control-advanced-settings\",\n  \"domain\" : {\n    \"uid\" : \"1e294ce0-367a-11e3-aa6e-0800200c9a66\",\n    \"name\" : \"Global\",\n    \"domain-type\" : \"global domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1678797069680,\n      \"iso-8601\" : \"2023-03-14T14:31+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1675751239124,\n      \"iso-8601\" : \"2023-02-07T08:27+0200\"\n    },\n    \"creator\" : \"System\"\n  },\n  \"available-actions\" : { },\n  \"read-only\" : true,\n  \"web-browsing-services\" : [ {\n    \"uid\" : \"97aeb3d4-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"http\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"forest green\",\n    \"port\" : \"80\"\n  }, {\n    \"uid\" : \"8eddeaa0-259d-448f-95b6-490a39f55962\",\n    \"name\" : \"HTTP_proxy\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"orange\",\n    \"port\" : \"8080\"\n  }, {\n    \"uid\" : \"704fbf04-1714-49a1-a750-38c0e4139a11\",\n    \"name\" : \"HTTPS_proxy\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Protocols/HTTP\",\n    \"color\" : \"navy blue\",\n    \"port\" : \"8080\"\n  }, {\n    \"uid\" : \"97aeb44f-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"AOL\",\n    \"type\" : \"service-tcp\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Services/TCPService\",\n    \"color\" : \"red\",\n    \"port\" : \"5190\"\n  }, {\n    \"uid\" : \"97aeb422-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"AH\",\n    \"type\" : \"service-other\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Services/OtherService\",\n    \"color\" : \"cyan\"\n  } ],\n  \"match-application-on-any-port\" : true,\n  \"domain-level-permission\" : false\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:16.040483",
    "source_file": "set-app-control-advanced-settings.html"
  }
}
```