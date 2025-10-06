# show-gateway-capabilities

```json
{
  "command": "show-gateway-capabilities",
  "description": "Show supported Check Point Gateway capabilities such as versions, hardware, platforms and blades.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-gateway-capabilities",
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
        "name": "hardware",
        "description": "Check Point hardware.",
        "type": "string",
        "required": false
      },
      {
        "name": "hardware-subtype",
        "description": "Gateway type (relevant only for Spark gateways).",
        "type": "string",
        "required": false,
        "valid_values": [
          "wired",
          "dsl",
          "wireless",
          "wireless + dsl",
          "wifi-lte"
        ]
      },
      {
        "name": "platform",
        "description": "Check Point gateway platform.",
        "type": "string",
        "required": false,
        "valid_values": [
          "smb",
          "quantum",
          "maestro",
          "elasticxl",
          "vsnext",
          "open server",
          "other"
        ]
      },
      {
        "name": "version",
        "description": "Gateway platform version.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "restrictions",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "wired",
          "dsl",
          "wireless",
          "wireless + dsl",
          "wifi-lte"
        ]
      },
      {
        "name": "hardware",
        "description": "Check Point hardware.",
        "type": "string",
        "required": false
      },
      {
        "name": "hardware-subtype",
        "description": "Gateway type (relevant only for Spark gateways).",
        "type": "string",
        "required": false,
        "valid_values": [
          "wired",
          "dsl",
          "wireless",
          "wireless + dsl",
          "wifi-lte"
        ]
      },
      {
        "name": "platform",
        "description": "Check Point gateway platform.",
        "type": "string",
        "required": false,
        "valid_values": [
          "smb",
          "quantum",
          "maestro",
          "elasticxl",
          "vsnext",
          "open server",
          "other"
        ]
      },
      {
        "name": "version",
        "description": "Gateway platform version.",
        "type": "string",
        "required": false
      },
      {
        "name": "supported-blades",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "management",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "name",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "readonly",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "network-security",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "name",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "readonly",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-prevention",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "autonomous",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "name",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "readonly",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "custom",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "name",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "readonly",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "supported-firmware-platforms",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "Default gateway firmware platform.",
        "type": "string",
        "required": false
      },
      {
        "name": "firmwarePlatforms",
        "description": "List of gateway firmware platforms.",
        "type": "array",
        "required": false
      },
      {
        "name": "supported-hardware",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "Default hardware.",
        "type": "string",
        "required": false
      },
      {
        "name": "hardware",
        "description": "List of Check Point hardware.",
        "type": "array",
        "required": false
      },
      {
        "name": "supported-hardware-subtypes",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "Default hardware subtype.",
        "type": "string",
        "required": false
      },
      {
        "name": "hardware-subtypes",
        "description": "List of Check Point hardware subtypes.",
        "type": "array",
        "required": false
      },
      {
        "name": "supported-platforms",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "smb",
          "quantum",
          "maestro",
          "elasticxl",
          "vsnext",
          "open server",
          "other"
        ]
      },
      {
        "name": "default",
        "description": "Default platform.",
        "type": "string",
        "required": false,
        "valid_values": [
          "smb",
          "quantum",
          "maestro",
          "elasticxl",
          "vsnext",
          "open server",
          "other"
        ]
      },
      {
        "name": "platforms",
        "description": "List of Check Point gateway platforms.",
        "type": "array",
        "required": false
      },
      {
        "name": "supported-versions",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "default",
        "description": "Default gateway platform version.",
        "type": "string",
        "required": false
      },
      {
        "name": "versions",
        "description": "List of gateway platform versions.",
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
    "show-gateway-capabilities for platform smb": {
      "description": "Show supported gateway capabilities for a specified platform",
      "request": "POST {{server}}/show-gateway-capabilities\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"platform\" : \"smb\"\n}",
      "response": "{\n  \"restrictions\" : {\n    \"platform\" : \"smb\",\n    \"version\" : \"any\",\n    \"hardware\" : \"any\"\n  },\n  \"supported-platforms\" : {\n    \"platforms\" : [ \"smb\" ],\n    \"default\" : \"smb\"\n  },\n  \"supported-versions\" : {\n    \"versions\" : [ \"R75.20\", \"R77.20\", \"R80.20\", \"R81.10\" ],\n    \"default\" : \"R81.10\"\n  },\n  \"supported-blades\" : {\n    \"network-security\" : [ {\n      \"name\" : \"Dynamic Routing\",\n      \"readonly\" : true,\n      \"default\" : true\n    }, {\n      \"name\" : \"QoS\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Application Control\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"SecureXL\",\n      \"readonly\" : true,\n      \"default\" : true\n    }, {\n      \"name\" : \"Anti-Spam & Email Security\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"IPSec VPN\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"URL Filtering\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Identity Awareness\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Firewall\",\n      \"readonly\" : false,\n      \"default\" : true\n    } ],\n    \"threat-prevention\" : {\n      \"custom\" : [ {\n        \"name\" : \"Threat Extraction\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Anti-Bot\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Threat Emulation\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Zero Phishing\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Anti-Virus\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"IPS\",\n        \"readonly\" : false,\n        \"default\" : false\n      } ],\n      \"autonomous\" : [ ]\n    }\n  },\n  \"supported-hardware\" : {\n    \"hardware\" : [ \"1100 Appliances\", \"1200R Appliances\", \"1430/1450 Appliances\", \"1470/1490 Appliances\", \"1530/1550 Appliances\", \"1570/1590 Appliances\", \"1570R Appliances\", \"1600 Appliances\", \"1800 Appliances\", \"Quantum Edge\" ],\n    \"default\" : \"1100 Appliances\"\n  }\n}"
    },
    "show-gateway-capabilities for version R81.20": {
      "description": "Show supported gateway capabilities for a specified version",
      "request": "POST {{server}}/show-gateway-capabilities\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"version\" : \"R81.20\"\n}",
      "response": "{\n  \"restrictions\" : {\n    \"version\" : \"R81.20\",\n    \"hardware\" : \"any\"\n  },\n  \"supported-platforms\" : {\n    \"platforms\" : [ \"quantum\", \"open server\", \"maestro\" ],\n    \"default\" : \"open server\"\n  },\n  \"supported-versions\" : {\n    \"versions\" : [ \"R81.20\" ],\n    \"default\" : \"R81.20\"\n  },\n  \"supported-blades\" : {\n    \"management\" : [ {\n      \"name\" : \"Identity Logging\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"Network Policy Management\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Endpoint Policy Management\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Compliance\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"Secondary Server\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"Logging & Status\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"SmartEvent Server\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"User Direct\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"Provisioning\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"SmartEvent Correlation Unit\",\n      \"readonly\" : true,\n      \"default\" : false\n    } ],\n    \"network-security\" : [ {\n      \"name\" : \"Dynamic Routing\",\n      \"readonly\" : true,\n      \"default\" : true\n    }, {\n      \"name\" : \"Mobile Access\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"SecureXL\",\n      \"readonly\" : true,\n      \"default\" : true\n    }, {\n      \"name\" : \"Anti-Spam & Email Security\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Content Awareness\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Identity Awareness\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Firewall\",\n      \"readonly\" : false,\n      \"default\" : true\n    }, {\n      \"name\" : \"Data Loss Protection\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"QoS\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Policy Server\",\n      \"readonly\" : true,\n      \"default\" : false\n    }, {\n      \"name\" : \"Application Control\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"IPSec VPN\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"URL Filtering\",\n      \"readonly\" : false,\n      \"default\" : false\n    }, {\n      \"name\" : \"Monitoring\",\n      \"readonly\" : false,\n      \"default\" : false\n    } ],\n    \"threat-prevention\" : {\n      \"custom\" : [ {\n        \"name\" : \"Threat Extraction\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Anti-Bot\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Threat Emulation\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Zero Phishing\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"Anti-Virus\",\n        \"readonly\" : false,\n        \"default\" : false\n      }, {\n        \"name\" : \"IPS\",\n        \"readonly\" : false,\n        \"default\" : false\n      } ],\n      \"autonomous\" : [ {\n        \"name\" : \"Sanitization (CDR)\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"C&C Protection\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"Threat Cloud\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"Zero Phishing\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"File & URL Reputation\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"Sandbox\",\n        \"readonly\" : false,\n        \"default\" : true\n      }, {\n        \"name\" : \"IPS Protections\",\n        \"readonly\" : false,\n        \"default\" : true\n      } ]\n    }\n  },\n  \"supported-hardware\" : {\n    \"hardware\" : [ \"2200 Appliance\", \"3000 Appliances\", \"4000 Appliances\", \"5000 Appliances\", \"6000 Appliances\", \"7000 Appliances\", \"12000 Appliances\", \"13000 Appliances\", \"15000 Appliances\", \"16000 Appliances\", \"21000 Appliances\", \"23000 Appliances\", \"26000 Appliances\", \"28000 Appliances\", \"QLS250 Quantum LightSpeed\", \"QLS450 Quantum LightSpeed\", \"QLS650 Quantum LightSpeed\", \"QLS800 Quantum LightSpeed\", \"MLS200 Maestro LightSpeed\", \"MLS400 Maestro LightSpeed\", \"Maestro\", \"CloudGuard IaaS\", \"CloudGuard for NSX\", \"Open Server\", \"Smart-1\" ],\n    \"default\" : \"Open Server\"\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:24.445717",
    "source_file": "show-gateway-capabilities.html"
  }
}
```