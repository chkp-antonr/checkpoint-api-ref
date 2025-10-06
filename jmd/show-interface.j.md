# show-interface

```json
{
  "command": "show-interface",
  "description": "Retrieve existing network interface using object uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-interface",
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
        "description": "Network interface uid.",
        "type": "string",
        "required": true
      },
      {
        "name": "gateway-uid",
        "description": "Gateway or cluster object uid that the interface belongs to. Required only if name was specified.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "name",
        "description": "Network interface name.",
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
        "name": "gateway",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "name",
        "description": "Gateway or cluster name.",
        "type": "string",
        "required": false
      },
      {
        "name": "type",
        "description": "Gateway or cluster type.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "Gateway or cluster object uid.",
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
        "name": "anti-spoofing",
        "description": "Enable anti-spoofing.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "cluster-members",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-mask-length",
        "description": "IPv4 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv4-network-mask",
        "description": "IPv4 network mask.",
        "type": "string",
        "required": false
      },
      {
        "name": "name",
        "description": "Cluster member interface name.",
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
        "name": "ipv6-mask-length",
        "description": "IPv6 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv6-network-mask",
        "description": "IPv6 network mask.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "Cluster member interface object UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "member-name",
        "description": "Cluster member object name.",
        "type": "string",
        "required": false
      },
      {
        "name": "member-uid",
        "description": "Cluster member object uid.",
        "type": "string",
        "required": false
      },
      {
        "name": "cluster-network-type",
        "description": "Cluster interface type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "cluster",
          "sync",
          "cluster + sync",
          "private"
        ]
      },
      {
        "name": "dynamic-ip",
        "description": "Enable dynamic interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 network address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-mask-length",
        "description": "IPv4 mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv4-network-mask",
        "description": "IPv4 network mask.",
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
        "name": "ipv6-mask-length",
        "description": "IPv6 mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv6-network-mask",
        "description": "IPv6 network mask.",
        "type": "string",
        "required": false
      },
      {
        "name": "monitored-by-cluster",
        "description": "When Private is selected as the Cluster interface type, cluster can monitor or not monitor the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "network-interface-type",
        "description": "Network Interface Type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "alias",
          "bond",
          "bridge",
          "bridge member",
          "ethernet",
          "loopback",
          "6 in 4 tunnel",
          "pppoe",
          "vpn tunnel",
          "vlan"
        ]
      },
      {
        "name": "security-zone-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "auto-calculated",
        "description": "Security Zone is calculated according to where the interface leads to.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-calculated-zone",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "auto-calculated-zone-uid",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "specific-security-zone-enabled",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "specific-zone",
        "description": "Security Zone specified manually.",
        "type": "string",
        "required": false
      },
      {
        "name": "specific-zone-uid",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "valid_values": [
          "automatic",
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-automatic",
        "description": "Topology configuration automatically calculated by get-interfaces command.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-manual",
        "description": "Topology configuration manually defined.",
        "type": "string",
        "required": false,
        "valid_values": [
          "automatic",
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "specific-network-uid",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "topology-settings-automatic",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "specific-network-uid",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "topology-settings-manual",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "specific-network-uid",
        "description": "N/A",
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
    "show network interface": {
      "description": "Show network interface.",
      "request": "POST {{server}}/show-interface\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"uid\" : \"f400bd09-381f-4435-b8f4-9e13338c6ad6\"\n}",
      "response": "{\n  \"uid\" : \"f400bd09-381f-4435-b8f4-9e13338c6ad6\",\n  \"name\" : \"eth0\",\n  \"type\" : \"interface\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"topology-settings-automatic\" : {\n    \"ip-address-behind-this-interface\" : \"not defined\",\n    \"interface-leads-to-dmz\" : false\n  },\n  \"topology-automatic\" : \"internal\",\n  \"topology-manual\" : \"internal\",\n  \"topology-settings-manual\" : {\n    \"ip-address-behind-this-interface\" : \"not defined\",\n    \"interface-leads-to-dmz\" : false\n  },\n  \"anti-spoofing-settings\" : {\n    \"action\" : \"detect\",\n    \"exclude-packets\" : false,\n    \"spoof-tracking\" : \"alert\"\n  },\n  \"network-interface-type\" : \"ethernet\",\n  \"security-zone-settings\" : {\n    \"auto-calculated-zone\" : \"InternalZone\",\n    \"auto-calculated-zone-uid\" : \"e8131db2-8388-42a5-924a-82de32db20f7\",\n    \"specific-zone-uid\" : \"237a4cbc-7fb6-4d50-872a-4904468271c4\",\n    \"specific-security-zone-enabled\" : true,\n    \"auto-calculated\" : false,\n    \"specific-zone\" : \"ExternalZone\"\n  },\n  \"anti-spoofing\" : false,\n  \"ipv4-address\" : \"1.12.33.11\",\n  \"ipv4-mask-length\" : 21,\n  \"gateway\" : {\n    \"type\" : \"simple-gateway\",\n    \"name\" : \"dummy-gw-1\",\n    \"uid\" : \"ff918e85-98c4-4b17-bcac-417aab863d87\"\n  },\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"tags\" : [ ],\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1685343307386,\n      \"iso-8601\" : \"2023-05-29T09:55+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1685343305189,\n      \"iso-8601\" : \"2023-05-29T09:55+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"read-only\" : false,\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"false\"\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:25.515147",
    "source_file": "show-interface.html"
  }
}
```