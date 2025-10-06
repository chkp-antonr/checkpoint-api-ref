# set-resource-uri

```json
{
  "command": "set-resource-uri",
  "description": "Edit existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-resource-uri",
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
        "name": "use-this-resource-to",
        "description": "Select the use of the URI resource.",
        "type": "string",
        "required": false,
        "default": "enforce_uri_capabilities",
        "valid_values": [
          "enforce_uri_capabilities",
          "optimize_url_logging",
          "enhance_ufp_performance"
        ]
      },
      {
        "name": "connection-methods",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "transparent",
        "description": "The security server is invisible to the client that originates the connection, and to the server. The Transparent connection method is the most secure.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "proxy",
        "description": "The Resource is applied when people specify the Check Point Security Gateway as a proxy in their browser.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "tunneling",
        "description": "The Resource is applied when people specify the Security Gateway as a proxy in their browser, and is used for connections where Security Gateway cannot examine the contents of the packets, not even the URL.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "uri-match-specification-type",
        "description": "The type can be Wild Cards or UFP, where a UFP server holds categories of forbidden web sites.",
        "type": "string",
        "required": false,
        "default": "wildcards",
        "valid_values": [
          "wildcards",
          "ufp"
        ]
      },
      {
        "name": "exception-track",
        "description": "Configures how to track connections that match this rule but fail the content security checks. An example of an exception is a connection with an unsupported scheme or method.",
        "type": "string",
        "required": false,
        "default": "none",
        "valid_values": [
          "none",
          "exception log",
          "exception alert"
        ]
      },
      {
        "name": "match-ufp",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "no_caching",
        "valid_values": [
          "security_gateway_one_request",
          "security_gateway_two_requests",
          "no_caching",
          "ufp_server"
        ]
      },
      {
        "name": "server",
        "description": "UFP server identified by name or UID. The UFP server must already be defined as an OPSEC Application.",
        "type": "string",
        "required": false
      },
      {
        "name": "caching-control",
        "description": "Specifies if and how caching is to be enabled.",
        "type": "string",
        "required": false,
        "default": "no_caching",
        "valid_values": [
          "security_gateway_one_request",
          "security_gateway_two_requests",
          "no_caching",
          "ufp_server"
        ]
      },
      {
        "name": "ignore-ufp-server-after-failure",
        "description": "The UFP server will be ignored after numerous UFP server connections were unsuccessful.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "number-of-failures-before-ignore",
        "description": "Signifies at what point the UFP server should be ignored.",
        "type": "integer",
        "required": false,
        "default": "0"
      },
      {
        "name": "timeout-before-reconnecting",
        "description": "The amount of time, in seconds, that must pass before a UFP server connection should be attempted.",
        "type": "integer",
        "required": false,
        "default": "0"
      },
      {
        "name": "match-wildcards",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "schemes",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "http",
        "description": "Http scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ftp",
        "description": "Ftp scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "gopher",
        "description": "Gopher scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "mailto",
        "description": "Mailto scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "news",
        "description": "News scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "wais",
        "description": "Wais scheme.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "other",
        "description": "You can specify another scheme in the Other field. You can use wildcards.",
        "type": "string",
        "required": false
      },
      {
        "name": "methods",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "get",
        "description": "GET method.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "post",
        "description": "POST method.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "head",
        "description": "HEAD method.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "put",
        "description": "PUT method.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "other",
        "description": "You can specify another method in the Other field. You can use wildcards.",
        "type": "string",
        "required": false
      },
      {
        "name": "host",
        "description": "The functionality of the Host parameter depends on the DNS setup of the addressed server. For the host, only the IP address or the full DNS name should be used.",
        "type": "string",
        "required": false
      },
      {
        "name": "path",
        "description": "Name matching is based on appending the file name in the request to the current working directory (unless the file name is already a full path name) and comparing the result to the path specified in the Resource definition.",
        "type": "string",
        "required": false
      },
      {
        "name": "query",
        "description": "The parameters that are sent to the URI when it is accessed.",
        "type": "string",
        "required": false
      },
      {
        "name": "action",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "replacement-uri",
        "description": "If the Action in a rule which uses this resource is Drop or Reject, then the Replacement URI is displayed instead of the one requested by the user.",
        "type": "string",
        "required": false
      },
      {
        "name": "strip-script-tags",
        "description": "Strip JAVA scripts.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "strip-applet-tags",
        "description": "Strip JAVA applets.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "strip-activex-tags",
        "description": "Strip activeX tags.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "strip-ftp-links",
        "description": "Strip ftp links.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "strip-port-strings",
        "description": "Strip ports.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "cvp",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "return_data_after_content_is_approved",
          "return_data_before_content_is_approved"
        ]
      },
      {
        "name": "enable-cvp",
        "description": "Select to enable the Content Vectoring Protocol.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "server",
        "description": "CVP server identified by name or UID. The CVP server must already be defined as an OPSEC Application.",
        "type": "string",
        "required": false
      },
      {
        "name": "allowed-to-modify-content",
        "description": "Configures the CVP server to inspect but not modify content.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "send-http-headers-to-cvp",
        "description": "Select, if you would like the CVP server to check the HTTP headers of the message packets.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "reply-order",
        "description": "Designates when the CVP server returns data to the Security Gateway security server.",
        "type": "string",
        "required": false,
        "default": "return_data_after_content_is_approved",
        "valid_values": [
          "return_data_after_content_is_approved",
          "return_data_before_content_is_approved"
        ]
      },
      {
        "name": "send-http-request-to-cvp",
        "description": "Used to protect against undesirable content in the HTTP request, for example, when inspecting peer-to-peer connections.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "send-only-unsafe-file-types",
        "description": "Improves the performance of the CVP server. This option does not send to the CVP server traffic that is considered safe.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "soap",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "allow_all_soap_requests",
        "valid_values": [
          "allow_all_soap_requests",
          "allow_soap_requests_as_specified_in_file"
        ]
      },
      {
        "name": "inspection",
        "description": "Allow all SOAP Requests, or Allow only SOAP requests specified in the following file-id.",
        "type": "string",
        "required": false,
        "default": "allow_all_soap_requests",
        "valid_values": [
          "allow_all_soap_requests",
          "allow_soap_requests_as_specified_in_file"
        ]
      },
      {
        "name": "file-id",
        "description": "A file containing SOAP requests.",
        "type": "string",
        "required": false,
        "valid_values": [
          "scheme1",
          "scheme2",
          "scheme3",
          "scheme4",
          "scheme5",
          "scheme6",
          "scheme7",
          "scheme8",
          "scheme9",
          "scheme10"
        ]
      },
      {
        "name": "track-connections",
        "description": "The method of tracking SOAP connections.",
        "type": "string",
        "required": false,
        "default": "none",
        "valid_values": [
          "none",
          "log",
          "popup_alert",
          "mail_alert",
          "snmp_trap_alert",
          "user_defined_alert_no",
          "user_defined_alert_no",
          "user_defined_alert_no"
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
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-this-resource-to",
        "description": "Select the use of the URI resource.",
        "type": "string",
        "required": false,
        "valid_values": [
          "enforce_uri_capabilities",
          "optimize_url_logging",
          "enhance_ufp_performance"
        ]
      },
      {
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "connection-methods",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "transparent",
        "description": "The security server is invisible to the client that originates the connection, and to the server. The Transparent connection method is the most secure.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy",
        "description": "The Resource is applied when people specify the Check Point Security Gateway as a proxy in their browser.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tunneling",
        "description": "The Resource is applied when people specify the Security Gateway as a proxy in their browser, and is used for connections where Security Gateway cannot examine the contents of the packets, not even the URL.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "uri-match-specification-type",
        "description": "The type can be Wild Cards or UFP, where a UFP server holds categories of forbidden web sites.",
        "type": "string",
        "required": false,
        "valid_values": [
          "wildcards",
          "ufp"
        ]
      },
      {
        "name": "exception-track",
        "description": "",
        "type": "Object",
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
        "name": "match-ufp",
        "description": "",
        "type": "Object",
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
        "name": "server",
        "description": "",
        "type": "Object",
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
        "name": "caching-control",
        "description": "Specifies if and how caching is to be enabled.",
        "type": "string",
        "required": false,
        "valid_values": [
          "security_gateway_one_request",
          "security_gateway_two_requests",
          "no_caching",
          "ufp_server"
        ]
      },
      {
        "name": "ignore-ufp-server-after-failure",
        "description": "The UFP server will be ignored after numerous UFP server connections were unsuccessful.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "number-of-failures-before-ignore",
        "description": "Signifies at what point the UFP server should be ignored.",
        "type": "integer",
        "required": false
      },
      {
        "name": "timeout-before-reconnecting",
        "description": "The amount of time, in seconds, that must pass before a UFP server connection should be attempted.",
        "type": "integer",
        "required": false
      },
      {
        "name": "match-wildcards",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "schemes",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "http",
        "description": "Http scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ftp",
        "description": "Ftp scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "gopher",
        "description": "Gopher scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mailto",
        "description": "Mailto scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "news",
        "description": "News scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "wais",
        "description": "Wais scheme.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "other",
        "description": "You can specify another scheme in the Other field. You can use wildcards.",
        "type": "string",
        "required": false
      },
      {
        "name": "methods",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "get",
        "description": "GET method.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "post",
        "description": "POST method.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "head",
        "description": "HEAD method.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "put",
        "description": "PUT method.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "other",
        "description": "You can specify another method in the Other field. You can use wildcards.",
        "type": "string",
        "required": false
      },
      {
        "name": "host",
        "description": "The functionality of the Host parameter depends on the DNS setup of the addressed server. For the host, only the IP address or the full DNS name should be used.",
        "type": "string",
        "required": false
      },
      {
        "name": "path",
        "description": "Name matching is based on appending the file name in the request to the current working directory (unless the file name is already a full path name) and comparing the result to the path specified in the Resource definition.",
        "type": "string",
        "required": false
      },
      {
        "name": "query",
        "description": "The parameters that are sent to the URI when it is accessed.",
        "type": "string",
        "required": false
      },
      {
        "name": "action",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "replacement-uri",
        "description": "If the Action in a rule which uses this resource is Drop or Reject, then the Replacement URI is displayed instead of the one requested by the user.",
        "type": "string",
        "required": false
      },
      {
        "name": "strip-script-tags",
        "description": "Strip JAVA scripts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "strip-applet-tags",
        "description": "Strip JAVA applets.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "strip-activex-tags",
        "description": "Strip activeX tags.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "strip-ftp-links",
        "description": "Strip ftp links.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "strip-port-strings",
        "description": "Strip ports.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cvp",
        "description": "",
        "type": "Object",
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
        "name": "enable-cvp",
        "description": "Select to enable the Content Vectoring Protocol.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "server",
        "description": "",
        "type": "Object",
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
        "name": "cvp-server-is-allowed-to-modify-content",
        "description": "Configures the CVP server to inspect but not modify content.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-http-headers-to-cvp",
        "description": "Select, if you would like the CVP server to check the HTTP headers of the message packets.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "reply-order",
        "description": "Designates when the CVP server returns data to the Security Gateway security server.",
        "type": "string",
        "required": false,
        "valid_values": [
          "return_data_after_content_is_approved",
          "return_data_before_content_is_approved"
        ]
      },
      {
        "name": "send-http-request-to-cvp",
        "description": "Used to protect against undesirable content in the HTTP request, for example, when inspecting peer-to-peer connections.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-only-unsafe-file-types",
        "description": "Improves the performance of the CVP server. This option does not send to the CVP server traffic that is considered safe.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "soap",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "allow_all_soap_requests",
          "allow_soap_requests_as_specified_in_file"
        ]
      },
      {
        "name": "inspection",
        "description": "Allow all SOAP Requests, or Allow only SOAP requests specified in the following file-id.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow_all_soap_requests",
          "allow_soap_requests_as_specified_in_file"
        ]
      },
      {
        "name": "file-id",
        "description": "A file containing SOAP requests.",
        "type": "string",
        "required": false,
        "valid_values": [
          "scheme1",
          "scheme2",
          "scheme3",
          "scheme4",
          "scheme5",
          "scheme6",
          "scheme7",
          "scheme8",
          "scheme9",
          "scheme10"
        ]
      },
      {
        "name": "track-connections",
        "description": "The method of tracking SOAP connections.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup_alert",
          "mail_alert",
          "snmp_trap_alert",
          "user_defined_alert_no",
          "user_defined_alert_no",
          "user_defined_alert_no"
        ]
      },
      {
        "name": "tags",
        "description": "Collection of tag objects identified by the name or UID.",
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
    "set-resource-uri": {
      "description": "",
      "request": "POST {{server}}/set-resource-uri\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"newUriResource\",\n  \"new-name\" : \"editedUriResource\",\n  \"use-this-resource-to\" : \"optimize_url_logging\",\n  \"connection-methods\" : {\n    \"transparent\" : \"false\",\n    \"tunneling\" : \"true\"\n  },\n  \"uri-match-specification-type\" : \"wildcards\",\n  \"match-wildcards\" : {\n    \"host\" : \"hostName\",\n    \"path\" : \"pathName\"\n  }\n}",
      "response": "{\n  \"uid\" : \"6781f656-575f-46f0-8be2-0bcb399d12b2\",\n  \"name\" : \"editedUriResource\",\n  \"type\" : \"resource-uri\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1661252100012,\n      \"iso-8601\" : \"2022-08-23T13:55+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1661243987400,\n      \"iso-8601\" : \"2022-08-23T11:39+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"available-actions\" : { },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Services/Resource\",\n  \"use-this-resource-to\" : \"optimize_url_logging\",\n  \"uri-match-specification-type\" : \"wildcards\",\n  \"exception-track\" : {\n    \"uid\" : \"97aeb47d-9aea-11d5-bd16-0090272ccb30\",\n    \"name\" : \"None\",\n    \"type\" : \"CpmiEmptyTrack\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"Track/tracksLog\"\n  },\n  \"connection-methods\" : {\n    \"transparent\" : false,\n    \"proxy\" : true,\n    \"tunneling\" : true\n  },\n  \"match-wildcards\" : {\n    \"host\" : \"hostName\",\n    \"path\" : \"pathName\",\n    \"query\" : \"*\",\n    \"schemes\" : {\n      \"http\" : false,\n      \"ftp\" : false,\n      \"gopher\" : false,\n      \"mailto\" : false,\n      \"news\" : false,\n      \"wais\" : false,\n      \"other\" : \"*\"\n    },\n    \"methods\" : {\n      \"get\" : false,\n      \"post\" : false,\n      \"head\" : false,\n      \"put\" : false,\n      \"other\" : \"*\"\n    }\n  },\n  \"action\" : {\n    \"strip-script-tags\" : false,\n    \"strip-applet-tags\" : false,\n    \"strip-activex-tags\" : false,\n    \"strip-ftp-links\" : false,\n    \"strip-port-strings\" : false\n  },\n  \"cvp\" : {\n    \"enable-cvp\" : false,\n    \"cvp-server-is-allowed-to-modify-content\" : true,\n    \"reply-order\" : \"return_data_after_content_is_approved\",\n    \"send-http-headers-to-cvp\" : false,\n    \"send-http-request-to-cvp\" : false,\n    \"send-only-unsafe-file-types\" : true\n  },\n  \"soap\" : {\n    \"inspection\" : \"allow_all_soap_requests\",\n    \"file-id\" : \"scheme1\",\n    \"track-connections\" : \"none\"\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:19.051785",
    "source_file": "set-resource-uri.html"
  }
}
```