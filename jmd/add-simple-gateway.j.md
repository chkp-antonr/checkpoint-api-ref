# add-simple-gateway

```json
{
  "command": "add-simple-gateway",
  "description": "Create new object.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-simple-gateway",
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "advanced-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "rematch-connections",
        "valid_values": [
          "keep-all-connections",
          "keep-data-connections",
          "rematch-connections"
        ]
      },
      {
        "name": "connection-persistence",
        "description": "Handling established connections when installing a new policy.",
        "type": "string",
        "required": false,
        "default": "rematch-connections",
        "valid_values": [
          "keep-all-connections",
          "keep-data-connections",
          "rematch-connections"
        ]
      },
      {
        "name": "sam",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "forward-to-other-sam-servers",
        "description": "Forward SAM clients' requests to other SAM servers.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-early-versions",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "enabled",
        "description": "Use early versions compatibility mode.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "compatibility-mode",
        "description": "Early versions compatibility mode.",
        "type": "string",
        "required": false,
        "default": "auth_opsec",
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "purge-sam-file",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "enabled",
        "description": "Purge SAM File.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "purge-when-size-reaches-to",
        "description": "Purge SAM File When it Reaches to.",
        "type": "integer",
        "required": false,
        "default": "100"
      },
      {
        "name": "anti-bot",
        "description": "Anti-Bot blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spam-and-email-security",
        "description": "Enables Anti-Spam & Email-Security blade.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-virus",
        "description": "Anti-Virus blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "application-control",
        "description": "Application Control blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "application-control-and-url-filtering-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "use_global_settings",
          "override_global"
        ]
      },
      {
        "name": "global-settings-mode",
        "description": "Whether to override global settings or not.",
        "type": "string",
        "required": false,
        "valid_values": [
          "use_global_settings",
          "override_global"
        ]
      },
      {
        "name": "override-global-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "allow_all_requests",
          "block_all_requests"
        ]
      },
      {
        "name": "fail-mode",
        "description": "Fail mode - allow or block all requests.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow_all_requests",
          "block_all_requests"
        ]
      },
      {
        "name": "website-categorization",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "mode",
        "description": "Website categorization mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "custom-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "social-networking-widgets",
        "description": "Social networking widgets mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "url-filtering",
        "description": "URL filtering mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "auto-generate-ip",
        "description": "Use an automatically generated IP address for the Gateway object (applies only to Smart-1 Cloud).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-topology-custom-recalculation-time",
        "description": "Auto topology custom recalculation time (seconds).",
        "type": "integer",
        "required": false,
        "default": "10"
      },
      {
        "name": "auto-topology-use-custom-recalculation-time",
        "description": "Auto topology to use custom recalculation time instead of default.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "communication-with-servers-behind-nat",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "according-to-topology",
        "valid_values": [
          "according-to-topology",
          "original-ip-only",
          "translated-ip-only"
        ]
      },
      {
        "name": "override-profile",
        "description": "Whether to override the Server (Check Point Host) object configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "according-to-topology: Use the original or translated IP address of the server based on the Topology of Security Gateway interfaces.original-ip-only: Use only the original IP address of the servertranslated-ip-only: Use only the translated IP address of the server.",
        "type": "string",
        "required": false,
        "default": "according-to-topology",
        "valid_values": [
          "according-to-topology",
          "original-ip-only",
          "translated-ip-only"
        ]
      },
      {
        "name": "content-awareness",
        "description": "Content Awareness blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "data-loss-prevention",
        "description": "Data Loss Prevention blade.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "enable-https-inspection",
        "description": "Enable HTTPS Inspection after defining an outbound inspection certificate. To define the outbound certificate use outbound inspection certificate API.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "fetch-policy",
        "description": "Security management server(s) to fetch the policy from.",
        "type": "string",
        "required": false
      },
      {
        "name": "firewall",
        "description": "Firewall blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "firewall-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "auto-calculate-connections-hash-table-size-and-memory-pool",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-maximum-limit-for-concurrent-connections",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "connections-hash-size",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-limit-for-concurrent-connections",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-memory-pool-size",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-pool-size",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "hardware",
        "description": "Gateway platform hardware type.",
        "type": "string",
        "required": false
      },
      {
        "name": "hit-count",
        "description": "Hit count tracks the number of connections each rule matches.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "https-inspection",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "bypass-on-client-failure",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "bypass-on-failure",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "bypass-under-load",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "value",
        "description": "* true - enabled.* false - disabled (default value).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "site-categorization-allow-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "string",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "deny-untrusted-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "deny-revoked-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "deny-expired-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "outbound-certificate",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.Identified by Name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "deployment-mode",
        "description": "* Full inspection - According to the configured HTTPS Inspection policy.* Learning mode - Inspect a small percentage of the traffic to identify issues and estimate the expected resource consumption of the configured HTTPS Inspection policy.",
        "type": "string",
        "required": false,
        "valid_values": [
          "full",
          "learning"
        ]
      },
      {
        "name": "icap-server",
        "description": "ICAP Server enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-awareness",
        "description": "Identity awareness blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-awareness-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "identity provider",
          "radius"
        ]
      },
      {
        "name": "browser-based-authentication",
        "description": "Enable Browser Based Authentication source.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "browser-based-authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "identity provider",
          "radius"
        ]
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "identity provider",
          "radius"
        ]
      },
      {
        "name": "authentication-method",
        "description": "Authentication method.",
        "type": "string",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "identity provider",
          "radius"
        ]
      },
      {
        "name": "identity-provider",
        "description": "Identity provider object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"identity provider\".",
        "type": "string",
        "required": false
      },
      {
        "name": "radius",
        "description": "Radius server object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"radius\".",
        "type": "string",
        "required": false
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "External user profile.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "internal-users",
        "description": "Internal users.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "users-from-external-directories",
        "description": "Users from external directories.",
        "type": "string",
        "required": false,
        "default": "all gateways directories",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "string",
        "required": false
      },
      {
        "name": "browser-based-authentication-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "base64-certificate",
        "description": "The certificate file encoded in Base64 with padding. This file must be in the *.p12 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "base64-password",
        "description": "Password (encoded in Base64 with padding) for the certificate file.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-agent",
        "description": "Enable Identity Agent source.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-agent-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "5",
        "valid_values": [
          "username and password",
          "defined on user record",
          "radius"
        ]
      },
      {
        "name": "agents-interval-keepalive",
        "description": "Agents send keepalive period (minutes).",
        "type": "integer",
        "required": false,
        "default": "5"
      },
      {
        "name": "user-reauthenticate-interval",
        "description": "Agent reauthenticate time interval (minutes).",
        "type": "integer",
        "required": false,
        "default": "480"
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "radius"
        ]
      },
      {
        "name": "authentication-method",
        "description": "Authentication method.",
        "type": "string",
        "required": false,
        "default": "username and password",
        "valid_values": [
          "username and password",
          "defined on user record",
          "radius"
        ]
      },
      {
        "name": "radius",
        "description": "Radius server object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"radius\".",
        "type": "string",
        "required": false
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "External user profile.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "internal-users",
        "description": "Internal users.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "users-from-external-directories",
        "description": "Users from external directories.",
        "type": "string",
        "required": false,
        "default": "all gateways directories",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "string",
        "required": false
      },
      {
        "name": "identity-agent-portal-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-based-enforcement",
        "description": "ON: Configures this object as a PEP-only object - identity-based enforcement (PEP) is enabled.OFF: Configures this object as a PDP-only object - identity-based enforcement is disabled.",
        "type": "string",
        "required": false,
        "default": "on",
        "valid_values": [
          "on",
          "off"
        ]
      },
      {
        "name": "identity-collector",
        "description": "Enable Identity Collector source.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-collector-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authorized-clients",
        "description": "",
        "type": "Object",
        "required": true
      },
      {
        "name": "client",
        "description": "Host / Network Group Name or UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "client-secret",
        "description": "Client Secret.",
        "type": "string",
        "required": true
      },
      {
        "name": "client",
        "description": "Host / Network Group Name or UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "client-secret",
        "description": "Client Secret.",
        "type": "string",
        "required": true
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "External user profile.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "internal-users",
        "description": "Internal users.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "users-from-external-directories",
        "description": "Users from external directories.",
        "type": "string",
        "required": false,
        "default": "all gateways directories",
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "string",
        "required": false
      },
      {
        "name": "client-access-permissions",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-sharing-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "1-2880"
        ]
      },
      {
        "name": "share-with-other-gateways",
        "description": "Enable identity sharing with other gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "receive-from-other-gateways",
        "description": "Enable receiving identity from other gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "receive-from",
        "description": "Gateway(s) to receive identity from.",
        "type": "string",
        "required": false
      },
      {
        "name": "cache-mode",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-mode-duration",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "1-2880"
        ]
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.Required only for 'override-profile' is True.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-2880"
        ]
      },
      {
        "name": "proxy-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "detect-using-x-forward-for",
        "description": "Whether to use X-Forward-For HTTP header, which is added by the proxy server to keep track of the original source IP.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "remote-access",
        "description": "Enable Remote Access Identity source.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "N/A",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "prevent",
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
        "default": "prevent",
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
        "default": "log",
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "dynamic-ip",
        "description": "The Topology of interface with Dynamic IP is set to Automatic - External.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "security-zone",
        "description": "N/A",
        "type": "boolean",
        "required": false,
        "default": "false"
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
        "name": "topology",
        "description": "N/A",
        "type": "string",
        "required": false,
        "default": "automatic",
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
        "default": "not defined",
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
        "default": "not defined",
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
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "Object",
        "required": false
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "interfaces-topology-settings",
        "description": "Topology setting for all interfaces on a Security Gateway. Default for Security Gateways that run Gaia OS: 'per interface'. Default for Quantum Spark gateways that run Gaia Embedded OS: 'global and automatic'. Changing this setting is supported only for Quantum Spark gateways.",
        "type": "string",
        "required": false,
        "valid_values": [
          "global and automatic",
          "per interface"
        ]
      },
      {
        "name": "ips",
        "description": "Intrusion Prevention System blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ips-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "bypass-all-under-load",
        "description": "Disable/enable all IPS protections until CPU and memory levels are back to normal.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "bypass-track-method",
        "description": "Track options when all IPS protections are disabled until CPU/memory levels are back to normal.",
        "type": "string",
        "required": false,
        "default": "alert",
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "activation-mode",
        "description": "Defines whether the IPS blade operates in Detect Only mode or enforces the configured IPS Policy.",
        "type": "string",
        "required": false,
        "default": "according-to-policy",
        "valid_values": [
          "according-to-policy",
          "detect-only"
        ]
      },
      {
        "name": "cpu-usage-low-threshold",
        "description": "CPU usage low threshold percentage (1-99).",
        "type": "integer",
        "required": false,
        "default": "70"
      },
      {
        "name": "cpu-usage-high-threshold",
        "description": "CPU usage high threshold percentage (1-99).",
        "type": "integer",
        "required": false,
        "default": "90"
      },
      {
        "name": "memory-usage-low-threshold",
        "description": "Memory usage low threshold percentage (1-99).",
        "type": "integer",
        "required": false,
        "default": "70"
      },
      {
        "name": "memory-usage-high-threshold",
        "description": "Memory usage high threshold percentage (1-99).",
        "type": "integer",
        "required": false,
        "default": "90"
      },
      {
        "name": "send-threat-cloud-info",
        "description": "Help improve Check Point Threat Prevention product by sending anonymous information.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ips-update-policy",
        "description": "Specifies whether the IPS will be downloaded from the Management or directly to the Gateway.",
        "type": "string",
        "required": false,
        "default": "gateway automatic update",
        "valid_values": [
          "via management",
          "gateway automatic update"
        ]
      },
      {
        "name": "mobile-access",
        "description": "Mobile Access blade.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "monitoring",
        "description": "Enables Real Time Monitoring blade.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "nat-hide-internal-interfaces",
        "description": "Hide internal networks behind the Gateway's external IP.",
        "type": "boolean",
        "required": false
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
        "name": "one-time-password",
        "description": "Shared password to establish SIC between the Security Management and the Security Gateway.",
        "type": "string",
        "required": false
      },
      {
        "name": "os-name",
        "description": "Gateway platform operating system.",
        "type": "string",
        "required": false
      },
      {
        "name": "platform-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "base64-certificate",
        "description": "The certificate file encoded in Base64 with padding. This file must be in the *.p12 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "base64-password",
        "description": "Password (encoded in Base64 with padding) for the certificate file.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-custom-proxy",
        "description": "Use custom proxy settings for this network object.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "proxy-server",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "N/A",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "qos",
        "description": "QoS.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-counters-report",
        "description": "Enables monitoring blades system counters report (e.g CPU Usage,Memory Usage).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-traffic-report",
        "description": "Enables monitoring blades traffic report.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-traffic-report-per-connection",
        "description": "Enables Monitoring blade traffic report per connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "save-logs-locally",
        "description": "Save logs locally on the gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-alerts-to-server",
        "description": "Server(s) to send alerts to.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-logs-to-backup-server",
        "description": "Backup server(s) to send logs to.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-logs-to-server",
        "description": "Server(s) to send logs to.",
        "type": "string",
        "required": false
      },
      {
        "name": "sic-name",
        "description": "Secure Internal Communication name.",
        "type": "string",
        "required": false
      },
      {
        "name": "threat-emulation",
        "description": "Threat Emulation blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-extraction",
        "description": "Threat Extraction blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-prevention-mode",
        "description": "The mode of Threat Prevention to use. When using Autonomous Threat Prevention, disabling the Threat Prevention blades is not allowed.",
        "type": "string",
        "required": false,
        "default": "custom",
        "valid_values": [
          "autonomous",
          "custom"
        ]
      },
      {
        "name": "url-filtering",
        "description": "URL Filtering blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "usercheck-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "enabled",
        "description": "State of the web portal (enabled or disabled). The supported blades are: {'Application Control', 'URL Filtering', 'Data Loss Prevention', 'Anti Virus', 'Anti Bot', 'Threat Emulation', 'Threat Extraction', 'Data Awareness'}.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "base64-certificate",
        "description": "The certificate file encoded in Base64 with padding. This file must be in the *.p12 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "base64-password",
        "description": "Password (encoded in Base64 with padding) for the certificate file.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "version",
        "description": "Gateway platform version.",
        "type": "string",
        "required": false,
        "default": "R82"
      },
      {
        "name": "vpn",
        "description": "VPN blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-settings",
        "description": "",
        "type": "array",
        "required": false,
        "default": "manual",
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "authentication",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "authentication-clients",
        "description": "Collection of VPN Authentication clients identified by the name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificates",
        "description": "",
        "type": "array",
        "required": false,
        "default": "manual",
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "name",
        "description": "Certificate name.",
        "type": "string",
        "required": true
      },
      {
        "name": "certificate-authority",
        "description": "Certificate authority to enroll from. Identified by the Name or UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "enrollment",
        "description": "",
        "type": "array",
        "required": true,
        "default": "manual",
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "enrollment-settings",
        "description": "",
        "type": "array",
        "required": true,
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "distinguished-name",
        "description": "The Distinguished Name of the certificate. If the certificate-authority type is \"external\", the Distinguished Name must start with \"CN=\".",
        "type": "string",
        "required": true
      },
      {
        "name": "alternate-names",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "name-type",
        "description": "Alternate name type.",
        "type": "string",
        "required": true,
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "value",
        "description": "Alternate name value.",
        "type": "string",
        "required": true
      },
      {
        "name": "name-type",
        "description": "Alternate name type.",
        "type": "string",
        "required": true,
        "valid_values": [
          "dn",
          "email",
          "fqdn",
          "ip address"
        ]
      },
      {
        "name": "value",
        "description": "Alternate name value.",
        "type": "string",
        "required": true
      },
      {
        "name": "enrollment-type",
        "description": "Weather to enroll certificate manually or automatically. Editable only if the Certificate Authority's automatic enrollment is enabled.",
        "type": "string",
        "required": false,
        "default": "manual",
        "valid_values": [
          "manual",
          "automatic"
        ]
      },
      {
        "name": "stored-at",
        "description": "Store keys on Security Management Server or on the Gateway. Default value is \"management server\". On cluster object only \"management server\" is valid.",
        "type": "string",
        "required": false,
        "valid_values": [
          "management server",
          "gateway"
        ]
      },
      {
        "name": "link-selection",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "use-main-address",
        "valid_values": [
          "use-main-address",
          "use-selected-address-from-topology",
          "use-statically-nated-ip",
          "calculated-ip-based-on-topology",
          "dns-resolving-from-hostname",
          "dns-resolving-from-gateway-and-domain-name",
          "use-probing-with-high-availability",
          "use-probing-with-load-sharing",
          "use-one-time-probing"
        ]
      },
      {
        "name": "ip-selection",
        "description": "N/A",
        "type": "string",
        "required": false,
        "default": "use-main-address",
        "valid_values": [
          "use-main-address",
          "use-selected-address-from-topology",
          "use-statically-nated-ip",
          "calculated-ip-based-on-topology",
          "dns-resolving-from-hostname",
          "dns-resolving-from-gateway-and-domain-name",
          "use-probing-with-high-availability",
          "use-probing-with-load-sharing",
          "use-one-time-probing"
        ]
      },
      {
        "name": "dns-resolving-hostname",
        "description": "DNS Resolving Hostname. Must be set when \"ip-selection\" was selected to be \"dns-resolving-from-hostname\".",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "IP Address. Must be set when \"ip-selection\" was selected to be \"use-selected-address-from-topology\" or \"use-statically-nated-ip\".",
        "type": "string",
        "required": false
      },
      {
        "name": "maximum-concurrent-ike-negotiations",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-concurrent-tunnels",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "office-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "off",
        "valid_values": [
          "off",
          "specific-group",
          "all-users"
        ]
      },
      {
        "name": "mode",
        "description": "Office Mode Permissions. When selected to be \"off\", all the other definitions are irrelevant.",
        "type": "string",
        "required": false,
        "default": "off",
        "valid_values": [
          "off",
          "specific-group",
          "all-users"
        ]
      },
      {
        "name": "group",
        "description": "Group. Identified by name or UID. Must be set when \"office-mode-permissions\" was selected to be \"group\".",
        "type": "string",
        "required": false
      },
      {
        "name": "allocate-ip-address-from",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "manual",
          "automatic"
        ]
      },
      {
        "name": "radius-server",
        "description": "Radius server used to authenticate the user.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-allocate-method",
        "description": "Use Allocate Method.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "allocate-method",
        "description": "Using either Manual (IP Pool) or Automatic (DHCP). Must be set when \"use-allocate-method\" is true.",
        "type": "string",
        "required": false,
        "default": "manual",
        "valid_values": [
          "manual",
          "automatic"
        ]
      },
      {
        "name": "manual-network",
        "description": "Manual Network. Identified by name or UID. Must be set when \"allocate-method\" was selected to be \"manual\".",
        "type": "string",
        "required": false
      },
      {
        "name": "dhcp-server",
        "description": "DHCP Server. Identified by name or UID. Must be set when \"allocate-method\" was selected to be \"automatic\".",
        "type": "string",
        "required": false
      },
      {
        "name": "virtual-ip-address",
        "description": "Virtual IPV4 address for DHCP server replies. Must be set when \"allocate-method\" was selected to be \"automatic\".",
        "type": "string",
        "required": false
      },
      {
        "name": "dhcp-mac-address",
        "description": "Calculated MAC address for DHCP allocation. Must be set when \"allocate-method\" was selected to be \"automatic\".",
        "type": "string",
        "required": false,
        "default": "per-machine",
        "valid_values": [
          "per-machine",
          "per-user"
        ]
      },
      {
        "name": "optional-parameters",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-primary-dns-server",
        "description": "Use Primary DNS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "primary-dns-server",
        "description": "Primary DNS Server. Identified by name or UID. Must be set when \"use-primary-dns-server\" is true and can not be set when \"use-primary-dns-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-first-backup-dns-server",
        "description": "Use First Backup DNS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "first-backup-dns-server",
        "description": "First Backup DNS Server. Identified by name or UID. Must be set when \"use-first-backup-dns-server\" is true and can not be set when \"use-first-backup-dns-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-second-backup-dns-server",
        "description": "Use Second Backup DNS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "second-backup-dns-server",
        "description": "Second Backup DNS Server. Identified by name or UID. Must be set when \"use-second-backup-dns-server\" is true and can not be set when \"use-second-backup-dns-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "dns-suffixes",
        "description": "DNS Suffixes.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-primary-wins-server",
        "description": "Use Primary WINS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "primary-wins-server",
        "description": "Primary WINS Server. Identified by name or UID. Must be set when \"use-primary-wins-server\" is true and can not be set when \"use-primary-wins-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-first-backup-wins-server",
        "description": "Use First Backup WINS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "first-backup-wins-server",
        "description": "First Backup WINS Server. Identified by name or UID. Must be set when \"use-first-backup-wins-server\" is true and can not be set when \"use-first-backup-wins-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-second-backup-wins-server",
        "description": "Use Second Backup WINS Server.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "second-backup-wins-server",
        "description": "Second Backup WINS Server. Identified by name or UID. Must be set when \"use-second-backup-wins-server\" is true and can not be set when \"use-second-backup-wins-server\" is false.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-lease-duration",
        "description": "IP Lease Duration in Minutes. The value must be in the range 2-32767.",
        "type": "integer",
        "required": false
      },
      {
        "name": "support-multiple-interfaces",
        "description": "Support connectivity enhancement for gateways with multiple external interfaces.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "perform-anti-spoofing",
        "description": "Perform Anti-Spoofing on Office Mode addresses.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "anti-spoofing-additional-addresses",
        "description": "Additional IP Addresses for Anti-Spoofing. Identified by name or UID. Must be set when \"perform-anti-spoofings\" is true.",
        "type": "string",
        "required": false,
        "default": "None"
      },
      {
        "name": "remote-access",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "certificate",
          "md5"
        ]
      },
      {
        "name": "support-l2tp",
        "description": "Support L2TP (relevant only when office mode is active).",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "l2tp-auth-method",
        "description": "L2TP Authentication Method. Must be set when \"support-l2tp\" is true.",
        "type": "string",
        "required": false,
        "default": "md5",
        "valid_values": [
          "certificate",
          "md5"
        ]
      },
      {
        "name": "l2tp-certificate",
        "description": "L2TP Certificate. Must be set when \"l2tp-auth-method\" was selected to be \"certificate\". Insert \"defaultCert\" when you want to use the default certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "allow-vpn-clients-to-route-traffic",
        "description": "Allow VPN clients to route traffic.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "support-nat-traversal-mechanism",
        "description": "Support NAT traversal mechanism (UDP encapsulation).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "nat-traversal-service",
        "description": "Allocated NAT traversal UDP service. Identified by name or UID. Must be set when \"support-nat-traversal-mechanism\" is true.",
        "type": "string",
        "required": false,
        "default": "VPN1_IPSEC_encapsulation"
      },
      {
        "name": "support-visitor-mode",
        "description": "Support Visitor Mode.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "visitor-mode-service",
        "description": "TCP Service for Visitor Mode. Identified by name or UID. Must be set when \"support-visitor-mode\" is true.",
        "type": "string",
        "required": false,
        "default": "https"
      },
      {
        "name": "visitor-mode-interface",
        "description": "Interface for Visitor Mode. Must be set when \"support-visitor-mode\" is true. Insert IPV4 Address of existing interface or \"All IPs\" when you want all interfaces.",
        "type": "string",
        "required": false,
        "default": "All IPs"
      },
      {
        "name": "vpn-domain",
        "description": "Gateway VPN domain identified by the name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-domain-exclude-external-ip-addresses",
        "description": "Exclude the external IP addresses from the VPN domain of this Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-domain-type",
        "description": "Gateway VPN domain type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "addresses_behind_nat"
        ]
      },
      {
        "name": "zero-phishing",
        "description": "Zero Phishing blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "zero-phishing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "automatic",
          "manual"
        ]
      },
      {
        "name": "gateway-fqdn-mode",
        "description": "Manual Fqdn.",
        "type": "string",
        "required": false,
        "valid_values": [
          "automatic",
          "manual"
        ]
      },
      {
        "name": "manual-fqdn",
        "description": "Zero Phishing gateway FQDN.",
        "type": "string",
        "required": false
      },
      {
        "name": "logs-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "alert-when-free-disk-space-below",
        "description": "Enable alert when free disk space is below threshold.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "alert-when-free-disk-space-below-threshold",
        "description": "Alert when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "alert-when-free-disk-space-below-type",
        "description": "Alert when free disk space below type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "before-delete-keep-logs-from-the-last-days",
        "description": "Enable before delete keep logs from the last days.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "before-delete-keep-logs-from-the-last-days-threshold",
        "description": "Before delete keep logs from the last days threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "before-delete-run-script",
        "description": "Enable Before delete run script.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "before-delete-run-script-command",
        "description": "Before delete run script command.",
        "type": "string",
        "required": false
      },
      {
        "name": "delete-index-files-older-than-days",
        "description": "Enable delete index files older than days.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-index-files-older-than-days-threshold",
        "description": "Delete index files older than days threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "delete-index-files-when-index-size-above",
        "description": "Enable delete index files when index size above.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-index-files-when-index-size-above-threshold",
        "description": "Delete index files when index size above threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "delete-when-free-disk-space-below",
        "description": "Enable delete when free disk space below.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-when-free-disk-space-below-threshold",
        "description": "Delete when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "detect-new-citrix-ica-application-names",
        "description": "Enable detect new Citrix ICA application names.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "distribute-logs-between-all-active-servers",
        "description": "Distribute logs between all active servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server",
        "description": "Enable forward logs to log server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server-name",
        "description": "Forward logs to log server name.",
        "type": "string",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server-schedule-name",
        "description": "Forward logs to log server schedule name.",
        "type": "string",
        "required": false
      },
      {
        "name": "free-disk-space-metrics",
        "description": "Free disk space metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "mbytes",
          "percent"
        ]
      },
      {
        "name": "perform-log-rotate-before-log-forwarding",
        "description": "Enable perform log rotate before log forwarding.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "reject-connections-when-free-disk-space-below-threshold",
        "description": "Enable reject connections when free disk space below threshold.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "reserve-for-packet-capture-metrics",
        "description": "Reserve for packet capture metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "reserve-for-packet-capture-threshold",
        "description": "Reserve for packet capture threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "rotate-log-by-file-size",
        "description": "Enable rotate log by file size.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rotate-log-file-size-threshold",
        "description": "Log file size threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "rotate-log-on-schedule",
        "description": "Enable rotate log on schedule.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rotate-log-schedule-name",
        "description": "Rotate log schedule name.",
        "type": "string",
        "required": false
      },
      {
        "name": "stop-logging-when-free-disk-space-below",
        "description": "Enable stop logging when free disk space below.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "stop-logging-when-free-disk-space-below-threshold",
        "description": "Stop logging when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "turn-on-qos-logging",
        "description": "Enable turn on QoS Logging.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "update-account-log-every",
        "description": "Update account log in every amount of seconds.",
        "type": "integer",
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
        "name": "advanced-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "keep-all-connections",
          "keep-data-connections",
          "rematch-connections"
        ]
      },
      {
        "name": "connection-persistence",
        "description": "Handling established connections when installing a new policy.",
        "type": "string",
        "required": false,
        "valid_values": [
          "keep-all-connections",
          "keep-data-connections",
          "rematch-connections"
        ]
      },
      {
        "name": "sam",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "forward-to-other-sam-servers",
        "description": "Forward SAM clients' requests to other SAM servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-early-versions",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "enabled",
        "description": "Use early versions compatibility mode.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "compatibility-mode",
        "description": "Early versions compatibility mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ssl_clear_opsec",
          "opsec",
          "ssl_opsec",
          "auth_opsec"
        ]
      },
      {
        "name": "purge-sam-file",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "enabled",
        "description": "Purge SAM File.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "purge-when-size-reaches-to",
        "description": "Purge SAM File When it Reaches to.",
        "type": "integer",
        "required": false
      },
      {
        "name": "anti-bot",
        "description": "Anti-Bot blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spam-and-email-security",
        "description": "Anti-Spam & Email-Security blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-virus",
        "description": "Anti-Virus blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "application-control",
        "description": "Application Control blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "application-control-and-url-filtering-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "use_global_settings",
          "override_global"
        ]
      },
      {
        "name": "global-settings-mode",
        "description": "Whether to override global settings or not.",
        "type": "string",
        "required": false,
        "valid_values": [
          "use_global_settings",
          "override_global"
        ]
      },
      {
        "name": "override-global-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "allow_all_requests",
          "block_all_requests"
        ]
      },
      {
        "name": "fail-mode",
        "description": "Fail mode - allow or block all requests.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allow_all_requests",
          "block_all_requests"
        ]
      },
      {
        "name": "website-categorization",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "mode",
        "description": "Website categorization mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background",
          "custom"
        ]
      },
      {
        "name": "custom-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "social-networking-widgets",
        "description": "Social networking widgets mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "url-filtering",
        "description": "URL filtering mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hold",
          "background"
        ]
      },
      {
        "name": "auto-generate-ip",
        "description": "Use an automatically generated IP address for the Gateway object (applies only to Smart-1 Cloud).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-topology-custom-recalculation-time",
        "description": "Auto topology custom recalculation time (seconds).",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "auto-topology-use-custom-recalculation-time",
        "description": "Auto topology to use custom recalculation time instead of default.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "communication-with-servers-behind-nat",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "according-to-topology",
          "original-ip-only",
          "translated-ip-only"
        ]
      },
      {
        "name": "override-profile",
        "description": "Whether to override the Server (Check Point Host) object configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "according-to-topology: Use the original or translated IP address of the server based on the Topology of Security Gateway interfaces.original-ip-only: Use only the original IP address of the servertranslated-ip-only: Use only the translated IP address of the server.",
        "type": "string",
        "required": false,
        "valid_values": [
          "according-to-topology",
          "original-ip-only",
          "translated-ip-only"
        ]
      },
      {
        "name": "content-awareness",
        "description": "Content Awareness blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "data-loss-prevention",
        "description": "Data Loss Prevention.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dynamic-ip",
        "description": "Dynamic IP address.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-https-inspection",
        "description": "Enable HTTPS Inspection after defining an outbound inspection certificate. To define the outbound certificate use \"set outbound-inspection-certificate\".",
        "type": "boolean",
        "required": false
      },
      {
        "name": "externally-managed",
        "description": "Externally Managed Check Point Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "fetch-policy",
        "description": "Security management server(s) to fetch the policy from.",
        "type": "array",
        "required": false
      },
      {
        "name": "firewall",
        "description": "Firewall blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "firewall-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "auto-calculate-connections-hash-table-size-and-memory-pool",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-maximum-limit-for-concurrent-connections",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "connections-hash-size",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-limit-for-concurrent-connections",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-memory-pool-size",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-pool-size",
        "description": "N/A",
        "type": "integer",
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
        "name": "hardware",
        "description": "Gateway platform hardware type.",
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
        "name": "hit-count",
        "description": "Hit count tracks the number of connections each rule matches.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "https-inspection",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "bypass-on-client-failure",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "bypass-on-failure",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "bypass-under-load",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "value",
        "description": "* true - enabled.* false - disabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "site-categorization-allow-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "string",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "string",
        "required": false,
        "valid_values": [
          "background",
          "hold"
        ]
      },
      {
        "name": "deny-untrusted-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "deny-revoked-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "deny-expired-server-cert",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "outbound-certificate",
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
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
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
        "name": "value",
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
        "name": "deployment-mode",
        "description": "* Full inspection - According to the configured HTTPS Inspection policy.* Learning mode - Inspect a small percentage of the traffic to identify issues and estimate the expected resource consumption of the configured HTTPS Inspection policy.",
        "type": "string",
        "required": false,
        "valid_values": [
          "full",
          "learning"
        ]
      },
      {
        "name": "icap-server",
        "description": "ICAP Server enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-awareness",
        "description": "Identity awareness blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-awareness-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "ad-query",
        "description": "AD Query source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "browser-based-authentication",
        "description": "Browser Based Authentication source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "browser-based-authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authentication-method",
        "description": "Authentication method.",
        "type": "string",
        "required": false
      },
      {
        "name": "identity-provider",
        "description": "Identity provider object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"identity provider\".",
        "type": "array",
        "required": false
      },
      {
        "name": "radius",
        "description": "Radius server object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"radius\".",
        "type": "string",
        "required": false
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "internal-users",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "users-from-external-directories",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "array",
        "required": false
      },
      {
        "name": "browser-based-authentication-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "collecting-identities",
        "description": "This gateway collects identities.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-agent",
        "description": "Identity Agent source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-agent-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "agents-interval-keepalive",
        "description": "Agents send keepalive period (minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authentication-method",
        "description": "Authentication method.",
        "type": "string",
        "required": false
      },
      {
        "name": "radius",
        "description": "Radius server object identified by the name or UID. Must be set when \"authentication-method\" was selected to be \"radius\".",
        "type": "string",
        "required": false
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "internal-users",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "users-from-external-directories",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "array",
        "required": false
      },
      {
        "name": "identity-agent-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "user-reauthenticate-interval",
        "description": "Agent reauthenticate time interval (minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "identity-based-enforcement",
        "description": "ON: Configures this object as a PEP-only object - identity-based enforcement (PEP) is enabled.OFF: Configures this object as a PDP-only object - identity-based enforcement is disabled.",
        "type": "string",
        "required": false,
        "valid_values": [
          "on",
          "off"
        ]
      },
      {
        "name": "identity-collector",
        "description": "Identity Collector source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-collector-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "internal-users",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "users-from-external-directories",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "array",
        "required": false
      },
      {
        "name": "authorized-clients",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "client",
        "description": "Client Name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "client-access-permissions",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-sharing-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "share-with-other-gateways",
        "description": "Enable identity sharing with other gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "receive-from-other-gateways",
        "description": "Enable receiving identity from other gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "receive-from",
        "description": "Gateway(s) to receive identity from.",
        "type": "array",
        "required": false
      },
      {
        "name": "cache-mode",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-mode-duration",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "override-profile",
        "description": "Override profile of global configuration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "profile-value",
        "description": "Override profile value.",
        "type": "integer",
        "required": false
      },
      {
        "name": "value",
        "description": "Override value.",
        "type": "integer",
        "required": false
      },
      {
        "name": "identity-web-api",
        "description": "Identity Web API source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "identity-web-api-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "authentication-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "users-directories",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "external-user-profile",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "internal-users",
        "description": "N/A",
        "type": "boolean",
        "required": false
      },
      {
        "name": "users-from-external-directories",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "all gateways directories",
          "specific",
          "none"
        ]
      },
      {
        "name": "specific",
        "description": "LDAP AU objects identified by the name or UID. Must be set when \"users-from-external-directories\" was selected to be \"specific\".",
        "type": "array",
        "required": false
      },
      {
        "name": "authorized-clients",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "client",
        "description": "Client Name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "client-access-permissions",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "detect-using-x-forward-for",
        "description": "Whether X-Forward-For HTTP header is been used.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "radius-accounting",
        "description": "Radius Accounting source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "remote-access",
        "description": "Remote Access source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "terminal-servers",
        "description": "Terminal Servers source enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
        ]
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
        "description": "Interface name.",
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
        "name": "anti-spoofing",
        "description": "N/A",
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
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "dynamic-ip",
        "description": "Enable dynamic interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "icon",
        "description": "Object icon.",
        "type": "string",
        "required": false
      },
      {
        "name": "network-interface-type",
        "description": "Type of network interface.",
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
        "name": "security-zone",
        "description": "N/A",
        "type": "boolean",
        "required": false
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
        "name": "specific-zone",
        "description": "Security Zone specified manually.",
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
        "name": "topology-automatic-calculation",
        "description": "Shows the automatic topology calculation.",
        "type": "string",
        "required": false,
        "valid_values": [
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
        "name": "uid",
        "description": "Network interface object UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "interfaces-topology-settings",
        "description": "Topology setting for all interfaces on a Security Gateway. Default for Security Gateways that run Gaia OS: 'per interface'. Default for Quantum Spark gateways that run Gaia Embedded OS: 'global and automatic'. Changing this setting is supported only for Quantum Spark gateways.",
        "type": "string",
        "required": false,
        "valid_values": [
          "global and automatic",
          "per interface"
        ]
      },
      {
        "name": "ips",
        "description": "Intrusion Prevention System blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ips-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "according-to-policy",
          "detect-only"
        ]
      },
      {
        "name": "activation-mode",
        "description": "IPS activation mode: 'according-to-policy' or 'detect-only'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "according-to-policy",
          "detect-only"
        ]
      },
      {
        "name": "bypass-all-under-load",
        "description": "Disable/enable all IPS protections until CPU and memory levels are back to normal.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "bypass-track-method",
        "description": "Track options when all IPS protections are disabled until CPU/memory levels are back to normal.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "cpu-usage-high-threshold",
        "description": "CPU usage high threshold percentage (1-99).",
        "type": "integer",
        "required": false
      },
      {
        "name": "cpu-usage-low-threshold",
        "description": "CPU usage low threshold percentage (1-99).",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-usage-high-threshold",
        "description": "Memory usage high threshold percentage (1-99).",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-usage-low-threshold",
        "description": "Memory usage low threshold percentage (1-99).",
        "type": "integer",
        "required": false
      },
      {
        "name": "send-threat-cloud-info",
        "description": "Help improve Check Point Threat Prevention product by sending anonymous information.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ips-update-policy",
        "description": "Specifies whether the IPS will be downloaded from the Management or directly to the Gateway.",
        "type": "string",
        "required": false,
        "valid_values": [
          "via management",
          "gateway automatic update"
        ]
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
        "name": "legacy-url-filtering",
        "description": "Legacy URL Filtering enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-server",
        "description": "Logging & Status.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mobile-access",
        "description": "Mobile-Access blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "monitoring",
        "description": "Monitoring blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "nat-hide-internal-interfaces",
        "description": "Hide internal networks behind the Gateway's external IP.",
        "type": "boolean",
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
      },
      {
        "name": "network-policy-management",
        "description": "Management blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "os-name",
        "description": "Gateway platform operating system.",
        "type": "string",
        "required": false
      },
      {
        "name": "platform-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "enabled",
        "description": "State of the web portal (enabled or disabled).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "policy-server",
        "description": "Policy-Server blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "use-custom-proxy",
        "description": "Use custom proxy settings for this network object.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-server",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "qos",
        "description": "QoS.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-counters-report",
        "description": "Enables monitoring blades system counters report (e.g CPU Usage,Memory Usage).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-traffic-report",
        "description": "Enables monitoring blades traffic report.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rtm-traffic-report-per-connection",
        "description": "Enables Monitoring blade traffic report per connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "save-logs-locally",
        "description": "Save logs locally on the gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-alerts-to-server",
        "description": "Server(s) to send alerts to.",
        "type": "array",
        "required": false
      },
      {
        "name": "send-logs-to-backup-server",
        "description": "Backup server(s) to send logs to.",
        "type": "array",
        "required": false
      },
      {
        "name": "send-logs-to-server",
        "description": "Servers(s) to send logs to.",
        "type": "array",
        "required": false
      },
      {
        "name": "sic-message",
        "description": "Secure Internal Communication message.",
        "type": "string",
        "required": false
      },
      {
        "name": "sic-name",
        "description": "Secure Internal Communication name.",
        "type": "string",
        "required": false
      },
      {
        "name": "sic-state",
        "description": "Secure Internal Communication state.",
        "type": "string",
        "required": false,
        "valid_values": [
          "uninitialized",
          "initialized",
          "communicating",
          "not communicating",
          "unknown",
          "failed",
          "waiting_for_first_connection"
        ]
      },
      {
        "name": "threat-emulation",
        "description": "Threat Emulation blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-extraction",
        "description": "Threat Extraction blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "threat-prevention-mode",
        "description": "The mode of Threat Prevention to use. When using Autonomous Threat Prevention, disabling the Threat Prevention blades is not allowed.",
        "type": "string",
        "required": false,
        "valid_values": [
          "autonomous",
          "custom"
        ]
      },
      {
        "name": "url-filtering",
        "description": "URL Filtering blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "usercheck-portal-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "enabled",
        "description": "State of the web portal (enabled or disabled).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "portal-web-settings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "aliases",
        "description": "List of URL aliases that are redirected to the main portal URL.",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Optional: IP address for the web portal to use, if your DNS server fails to resolve the main portal URL. Note: If your DNS server resolves the main portal URL, this IP address is ignored.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-url",
        "description": "The main URL for the web portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "certificate",
        "description": "The certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-dn",
        "description": "The DN (Distinguished Name) of the certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-from",
        "description": "The date, from which the certificate is valid.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-valid-to",
        "description": "The certificate expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "accessibility",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "allow-access-from",
        "description": "Allowed access to the web portal (based on interfaces, or security policy).",
        "type": "string",
        "required": false,
        "valid_values": [
          "rule_base",
          "internal_interfaces",
          "all_interfaces"
        ]
      },
      {
        "name": "internal-access-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "undefined",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'Undefined'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dmz",
        "description": "Controls portal access settings for internal interfaces, whose topology is set to 'DMZ'.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn",
        "description": "Controls portal access settings for interfaces that are part of a VPN Encryption Domain.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "version",
        "description": "Gateway platform version.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn",
        "description": "VPN blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-settings",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "active",
          "backup"
        ]
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "active",
          "backup"
        ]
      },
      {
        "name": "interface-name",
        "description": "The name of the interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "next-hop-ip",
        "description": "The IP address of the next hop.",
        "type": "string",
        "required": false
      },
      {
        "name": "static-nat-ip",
        "description": "The NATed IPv4 address that hides the source IPv4 address of outgoing connections (applies only to IPv4).",
        "type": "string",
        "required": false
      },
      {
        "name": "priority",
        "description": "Priority of a 'Backup' interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "redundancy-mode",
        "description": "Interface redundancy mode (Active/Backup).",
        "type": "string",
        "required": false,
        "valid_values": [
          "active",
          "backup"
        ]
      },
      {
        "name": "ip-version",
        "description": "The IP version of the interface's IP address (IPv4/IPv6).",
        "type": "string",
        "required": false,
        "valid_values": [
          "ipv4",
          "ipv6"
        ]
      },
      {
        "name": "authentication",
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
        "name": "authentication-clients",
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
        "name": "certificates",
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
        "description": "Certificate name.",
        "type": "string",
        "required": false
      },
      {
        "name": "distinguished-name",
        "description": "The Distinguished Name of the certificate.",
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
        "name": "base64-certificate",
        "description": "Certificate file encoded in base64.",
        "type": "string",
        "required": false
      },
      {
        "name": "certificate-authority",
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
        "name": "expiration-date",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "iso-8601",
        "description": "Date and time represented in international ISO 8601 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "posix",
        "description": "Number of milliseconds that have elapsed since 00:00:00, 1 January 1970.",
        "type": "integer",
        "required": false
      },
      {
        "name": "status",
        "description": "Certificate status.",
        "type": "string",
        "required": false,
        "valid_values": [
          "signed",
          "unsigned"
        ]
      },
      {
        "name": "stored-at",
        "description": "Store keys on Security Management Server or on the Gateway. On cluster object only \"management server\" is valid.",
        "type": "string",
        "required": false,
        "valid_values": [
          "management server",
          "gateway"
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
        "name": "link-selection",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "use-main-address",
          "use-selected-address-from-topology",
          "use-statically-nated-ip",
          "calculated-ip-based-on-topology",
          "dns-resolving-from-hostname",
          "dns-resolving-from-gateway-and-domain-name",
          "use-probing-with-high-availability",
          "use-probing-with-load-sharing",
          "use-one-time-probing"
        ]
      },
      {
        "name": "ip-selection",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "use-main-address",
          "use-selected-address-from-topology",
          "use-statically-nated-ip",
          "calculated-ip-based-on-topology",
          "dns-resolving-from-hostname",
          "dns-resolving-from-gateway-and-domain-name",
          "use-probing-with-high-availability",
          "use-probing-with-load-sharing",
          "use-one-time-probing"
        ]
      },
      {
        "name": "dns-resolving-hostname",
        "description": "DNS Resolving Hostname. Must be set when \"ip-selection\" was selected to be \"dns-resolving-from-hostname\".",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "IP Address. Must be set when \"ip-selection\" was selected to be \"use-selected-address-from-topology\" or \"use-statically-nated-ip\".",
        "type": "string",
        "required": false
      },
      {
        "name": "maximum-concurrent-ike-negotiations",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "maximum-concurrent-tunnels",
        "description": "N/A",
        "type": "integer",
        "required": false
      },
      {
        "name": "office-mode",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "off",
          "specific-group",
          "all-users"
        ]
      },
      {
        "name": "mode",
        "description": "Office Mode Permissions. When selected to be \"off\", all the other definitions are irrelevant.",
        "type": "string",
        "required": false,
        "valid_values": [
          "off",
          "specific-group",
          "all-users"
        ]
      },
      {
        "name": "group",
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
        "name": "allocate-ip-address-from",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "manual",
          "automatic"
        ]
      },
      {
        "name": "radius-server",
        "description": "Radius server used to authenticate the user.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-allocate-method",
        "description": "Use Allocate Method.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allocate-method",
        "description": "Using either Manual (IP Pool) or Automatic (DHCP). Must be set when \"use-allocate-method\" is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "automatic"
        ]
      },
      {
        "name": "manual-network",
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
        "name": "dhcp-server",
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
        "name": "virtual-ip-address",
        "description": "Virtual IPV4 address for DHCP server replies. Must be set when \"allocate-method\" was selected to be \"automatic\".",
        "type": "string",
        "required": false
      },
      {
        "name": "dhcp-mac-address",
        "description": "Calculated MAC address for DHCP allocation. Must be set when \"allocate-method\" was selected to be \"automatic\".",
        "type": "string",
        "required": false,
        "valid_values": [
          "per-machine",
          "per-user"
        ]
      },
      {
        "name": "optional-parameters",
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
        "name": "use-primary-dns-server",
        "description": "Use Primary DNS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "primary-dns-server",
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
        "name": "use-first-backup-dns-server",
        "description": "Use First Backup DNS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "first-backup-dns-server",
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
        "name": "use-second-backup-dns-server",
        "description": "Use Second Backup DNS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "second-backup-dns-server",
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
        "name": "dns-suffixes",
        "description": "DNS Suffixes.",
        "type": "string",
        "required": false
      },
      {
        "name": "use-primary-wins-server",
        "description": "Use Primary WINS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "primary-wins-server",
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
        "name": "use-first-backup-wins-server",
        "description": "Use First Backup WINS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "first-backup-wins-server",
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
        "name": "use-second-backup-wins-server",
        "description": "Use Second Backup WINS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "second-backup-wins-server",
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
        "name": "ip-lease-duration",
        "description": "IP Lease Duration in Minutes. The value must be in the range 2-32767.",
        "type": "integer",
        "required": false
      },
      {
        "name": "support-multiple-interfaces",
        "description": "Support connectivity enhancement for gateways with multiple external interfaces.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "perform-anti-spoofing",
        "description": "Perform Anti-Spoofing on Office Mode addresses.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-additional-addresses",
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
        "name": "remote-access",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "certificate",
          "md5"
        ]
      },
      {
        "name": "support-l2tp",
        "description": "Support L2TP (relevant only when office mode is active).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "l2tp-auth-method",
        "description": "L2TP Authentication Method. Must be set when \"support-l2tp\" is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "certificate",
          "md5"
        ]
      },
      {
        "name": "l2tp-certificate",
        "description": "L2TP Certificate. Must be set when \"l2tp-auth-method\" was selected to be \"certificate\". Insert \"defaultCert\" when you want to use the default certificate.",
        "type": "string",
        "required": false
      },
      {
        "name": "allow-vpn-clients-to-route-traffic",
        "description": "Allow VPN clients to route traffic.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "support-nat-traversal-mechanism",
        "description": "Support NAT traversal mechanism (UDP encapsulation).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "nat-traversal-service",
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
        "name": "support-visitor-mode",
        "description": "Support Visitor Mode.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "visitor-mode-service",
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
        "name": "visitor-mode-interface",
        "description": "Interface for Visitor Mode. Must be set when \"support-visitor-mode\" is true. Insert IPV4 Address of existing interface or \"All IPs\" when you want all interfaces.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-domain",
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
        "name": "vpn-domain-exclude-external-ip-addresses",
        "description": "Exclude the external IP addresses from the VPN domain of this Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-domain-type",
        "description": "Gateway VPN domain type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "ranges",
          "addresses_behind_nat"
        ]
      },
      {
        "name": "zero-phishing",
        "description": "Zero Phishing blade enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "zero-phishing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "automatic",
          "manual"
        ]
      },
      {
        "name": "gateway-fqdn-mode",
        "description": "Manual Fqdn.",
        "type": "string",
        "required": false,
        "valid_values": [
          "automatic",
          "manual"
        ]
      },
      {
        "name": "manual-fqdn",
        "description": "Zero Phishing gateway FQDN.",
        "type": "string",
        "required": false
      },
      {
        "name": "logs-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "alert-when-free-disk-space-below",
        "description": "Alert when free disk space is below threshold enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "alert-when-free-disk-space-below-metrics",
        "description": "Alert when free disk space below metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "alert-when-free-disk-space-below-threshold",
        "description": "Alert when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "alert-when-free-disk-space-below-type",
        "description": "Alert when free disk space below type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "before-delete-keep-logs-from-the-last-days",
        "description": "Before delete keep logs from the last days enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "before-delete-keep-logs-from-the-last-days-threshold",
        "description": "Before delete keep logs from the last days threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "before-delete-run-script",
        "description": "Before delete run script enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "before-delete-run-script-command",
        "description": "Before delete run script command.",
        "type": "string",
        "required": false
      },
      {
        "name": "delete-index-files-older-than-days",
        "description": "Delete index files older than days enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-index-files-older-than-days-threshold",
        "description": "Delete index files older than days threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "delete-index-files-when-index-size-above",
        "description": "Delete index files when index size above enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-index-files-when-index-size-above-metrics",
        "description": "Delete index files when index size above metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "delete-index-files-when-index-size-above-threshold",
        "description": "Delete index files when index size above threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "delete-when-free-disk-space-below",
        "description": "Delete when free disk space below enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delete-when-free-disk-space-below-metrics",
        "description": "Delete when free disk space below metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "delete-when-free-disk-space-below-threshold",
        "description": "Delete when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "detect-new-citrix-ica-application-names",
        "description": "Detect new Citrix ICA application names enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "distribute-logs-between-all-active-servers",
        "description": "Distribute logs between all active servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server",
        "description": "Forward logs to log server enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server-name",
        "description": "Forward logs to log server name.",
        "type": "string",
        "required": false
      },
      {
        "name": "forward-logs-to-log-server-schedule-name",
        "description": "Forward logs to log server schedule name.",
        "type": "string",
        "required": false
      },
      {
        "name": "perform-log-rotate-before-log-forwarding",
        "description": "Perform log rotate before log forwarding enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "reject-connections-when-free-disk-space-below-threshold",
        "description": "Reject connections when free disk space below threshold enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "reserve-for-packet-capture-metrics",
        "description": "Reserve for packet capture metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "reserve-for-packet-capture-threshold",
        "description": "Reserve for packet capture threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "rotate-log-by-file-size",
        "description": "Rotate log by file size enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rotate-log-file-size-threshold",
        "description": "Log file size threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "rotate-log-on-schedule",
        "description": "Rotate log on schedule enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "rotate-log-schedule-name",
        "description": "Rotate log schedule name.",
        "type": "string",
        "required": false
      },
      {
        "name": "stop-logging-when-free-disk-space-below",
        "description": "Stop logging when free disk space below enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "stop-logging-when-free-disk-space-below-metrics",
        "description": "Stop logging when free disk space below metrics.",
        "type": "string",
        "required": false,
        "valid_values": [
          "percent",
          "mbytes"
        ]
      },
      {
        "name": "stop-logging-when-free-disk-space-below-threshold",
        "description": "Stop logging when free disk space below threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "turn-on-qos-logging",
        "description": "Turn on QoS Logging enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "update-account-log-every",
        "description": "Update account log in every amount of seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "smb-logs-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "alert-when-queue-is-full",
        "description": "Alert when queue is full enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "alert-when-queue-is-full-type",
        "description": "Alert when queue is full type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "detect-new-citrix-ica-application-names",
        "description": "Detect new citrix ica application names enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "stop-logging-when-queue-reaches-maximal-capacity",
        "description": "Stop logging when queue reaches maximal capacity enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "stop-logging-when-queue-reaches-maximal-capacity-threshold",
        "description": "Stop logging when queue reaches maximal capacity threshold.",
        "type": "integer",
        "required": false
      },
      {
        "name": "turn-on-qos-logging",
        "description": "Turn on qos logging enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "update-account-log-every",
        "description": "Update account log in every amount of seconds.",
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
    "add-simple-gateway": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"ip-address\" : \"192.0.2.1\"\n}",
      "response": "{\n  \"uid\" : \"99457705-dc26-40ce-b9cd-5633eb09b1aa\",\n  \"domain\" : {\n    \"domain-type\" : \"domain\",\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"read-only\" : false,\n    \"last-modify-time\" : {\n      \"posix\" : 1451485835851,\n      \"iso-8601\" : \"2015-12-30T16:30+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1451485835851,\n      \"iso-8601\" : \"2015-12-30T16:30+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"name\" : \"gw1\",\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"General/globalsNa\",\n  \"groups\" : [ ],\n  \"ipv6-address\" : \"::0\",\n  \"dynamic-ip\" : false,\n  \"version\" : \"R80\",\n  \"os-name\" : \"Gaia\",\n  \"hardware\" : \"Open server\",\n  \"sic-name\" : \"\",\n  \"sic-state\" : \"uninitialized\",\n  \"interfaces\" : [ ],\n  \"firewall\" : true,\n  \"firewall-settings\" : {\n    \"auto-maximum-limit-for-concurrent-connections\" : true,\n    \"maximum-limit-for-concurrent-connections\" : 25000,\n    \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n    \"connections-hash-size\" : 131072,\n    \"memory-pool-size\" : 6,\n    \"maximum-memory-pool-size\" : 30\n  },\n  \"vpn\" : false,\n  \"application-control\" : false,\n  \"url-filtering\" : false,\n  \"data-awareness\" : false,\n  \"ips\" : false,\n  \"anti-bot\" : false,\n  \"anti-virus\" : false,\n  \"threat-emulation\" : false,\n  \"save-logs-locally\" : false,\n  \"send-alerts-to-server\" : [ \"test_server_1\" ],\n  \"send-logs-to-server\" : [ \"test_server_2\" ],\n  \"send-logs-to-backup-server\" : [ ],\n  \"logs-settings\" : {\n    \"rotate-log-by-file-size\" : false,\n    \"rotate-log-file-size-threshold\" : 1000,\n    \"rotate-log-on-schedule\" : false,\n    \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"alert-when-free-disk-space-below\" : true,\n    \"alert-when-free-disk-space-below-threshold\" : 20,\n    \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n    \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"delete-when-free-disk-space-below\" : true,\n    \"delete-when-free-disk-space-below-threshold\" : 5000,\n    \"before-delete-keep-logs-from-the-last-days\" : false,\n    \"before-delete-keep-logs-from-the-last-days-threshold\" : 0,\n    \"before-delete-run-script\" : false,\n    \"before-delete-run-script-command\" : \"\",\n    \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"stop-logging-when-free-disk-space-below\" : true,\n    \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n    \"reject-connections-when-free-disk-space-below-threshold\" : false,\n    \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n    \"reserve-for-packet-capture-threshold\" : 500,\n    \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n    \"delete-index-files-when-index-size-above\" : false,\n    \"delete-index-files-when-index-size-above-threshold\" : 100000,\n    \"delete-index-files-older-than-days\" : true,\n    \"delete-index-files-older-than-days-threshold\" : 14,\n    \"forward-logs-to-log-server\" : false,\n    \"perform-log-rotate-before-log-forwarding\" : false,\n    \"update-account-log-every\" : 3600,\n    \"detect-new-citrix-ica-application-names\" : false,\n    \"turn-on-qos-logging\" : true\n  },\n  \"enable-https-inspection\" : false,\n  \"https-inspection\" : {\n    \"bypass-on-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"site-categorization-allow-mode\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : \"hold\"\n    },\n    \"deny-untrusted-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"deny-expired-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"outbound-certificate\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : {\n        \"uid\" : \"f215045c-a773-45c2-8f71-0ff3e25c3b2d\",\n        \"name\" : \"OutboundCertificate\",\n        \"type\" : \"outbound-inspection-certificate\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"subject_user_certificate\",\n        \"color\" : \"black\"\n      }\n    },\n    \"deny-revoked-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    }\n  }\n}"
    },
    "add-simple-gateway with fetch policy": {
      "description": "Fetch is done according to the order of the list",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"ipv4-address\" : \"192.0.2.230\",\n  \"fetch-policy\" : {\n    \"add\" : [ \"managementPri\", \"managementSec\" ]\n  }\n}",
      "response": ""
    },
    "add-simple-gateway with identity sharing": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw\",\n  \"ip-address\" : \"1.2.3.4\",\n  \"identity-awareness\" : true,\n  \"identity-awareness-settings\" : {\n    \"identity-agent\" : true,\n    \"identity-sharing-settings\" : {\n      \"share-with-other-gateways\" : false,\n      \"receive-from-other-gateways\" : true,\n      \"cache-mode\" : {\n        \"override-profile\" : true,\n        \"value\" : true\n      },\n      \"cache-mode-duration\" : {\n        \"override-profile\" : true,\n        \"value\" : 99\n      },\n      \"receive-from\" : \"IDServerGW\"\n    },\n    \"identity-based-enforcement\" : \"on\"\n  }\n}",
      "response": "{\n  \"uid\" : \"fe9a3751-8b3b-4ba9-a7c9-48a1d91d99a1\",\n  \"name\" : \"gw\",\n  \"type\" : \"simple-gateway\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1683792679980,\n      \"iso-8601\" : \"2023-05-11T11:11+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1683792679980,\n      \"iso-8601\" : \"2023-05-11T11:11+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : {\n    \"clone\" : \"not_supported\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"nat-settings\" : {\n    \"auto-rule\" : false\n  },\n  \"ipv4-address\" : \"1.9.3.9\",\n  \"dynamic-ip\" : false,\n  \"version\" : \"R82\",\n  \"os-name\" : \"Gaia\",\n  \"hardware\" : \"Open server\",\n  \"sic-name\" : \"\",\n  \"sic-state\" : \"uninitialized\",\n  \"interfaces\" : [ ],\n  \"network-policy-management\" : false,\n  \"log-server\" : false,\n  \"firewall\" : true,\n  \"firewall-settings\" : {\n    \"auto-maximum-limit-for-concurrent-connections\" : true,\n    \"maximum-limit-for-concurrent-connections\" : 25000,\n    \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n    \"connections-hash-size\" : 131072,\n    \"memory-pool-size\" : 6,\n    \"maximum-memory-pool-size\" : 30\n  },\n  \"vpn\" : false,\n  \"policy-server\" : false,\n  \"mobile-access\" : false,\n  \"application-control\" : false,\n  \"url-filtering\" : false,\n  \"legacy-url-filtering\" : false,\n  \"application-control-and-url-filtering-settings\" : {\n    \"global-settings-mode\" : \"use_global_settings\"\n  },\n  \"content-awareness\" : false,\n  \"monitoring\" : false,\n  \"anti-spam-and-email-security\" : false,\n  \"threat-prevention-mode\" : \"custom\",\n  \"ips\" : false,\n  \"anti-bot\" : false,\n  \"anti-virus\" : false,\n  \"threat-emulation\" : false,\n  \"threat-extraction\" : false,\n  \"zero-phishing\" : false,\n  \"ips-update-policy\" : \"gateway automatic update\",\n  \"identity-awareness\" : true,\n  \"data-loss-prevention\" : false,\n  \"qos\" : false,\n  \"externally-managed\" : false,\n  \"hit-count\" : true,\n  \"save-logs-locally\" : false,\n  \"send-alerts-to-server\" : [ \"mgmt_172.23.26.39-jaguar_155_global1MGMT\" ],\n  \"send-logs-to-server\" : [ \"mgmt_172.23.26.39-jaguar_155_global1MGMT\" ],\n  \"send-logs-to-backup-server\" : [ ],\n  \"logs-settings\" : {\n    \"rotate-log-by-file-size\" : false,\n    \"rotate-log-file-size-threshold\" : 1000,\n    \"rotate-log-on-schedule\" : false,\n    \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"alert-when-free-disk-space-below\" : true,\n    \"alert-when-free-disk-space-below-threshold\" : 20,\n    \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n    \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"delete-when-free-disk-space-below\" : true,\n    \"delete-when-free-disk-space-below-threshold\" : 5000,\n    \"before-delete-keep-logs-from-the-last-days\" : false,\n    \"before-delete-keep-logs-from-the-last-days-threshold\" : 3664,\n    \"before-delete-run-script\" : false,\n    \"before-delete-run-script-command\" : \"\",\n    \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"stop-logging-when-free-disk-space-below\" : true,\n    \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n    \"reject-connections-when-free-disk-space-below-threshold\" : false,\n    \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n    \"reserve-for-packet-capture-threshold\" : 500,\n    \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n    \"delete-index-files-when-index-size-above\" : false,\n    \"delete-index-files-when-index-size-above-threshold\" : 100000,\n    \"delete-index-files-older-than-days\" : false,\n    \"delete-index-files-older-than-days-threshold\" : 14,\n    \"forward-logs-to-log-server\" : false,\n    \"perform-log-rotate-before-log-forwarding\" : false,\n    \"update-account-log-every\" : 3600,\n    \"detect-new-citrix-ica-application-names\" : false,\n    \"turn-on-qos-logging\" : true,\n    \"distribute-logs-between-all-active-servers\" : false\n  },\n  \"platform-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"main-url\" : \"https://1.9.3.9/\",\n      \"ip-address\" : \"1.9.3.9\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"RULE_BASE\"\n    }\n  },\n  \"nat-hide-internal-interfaces\" : false,\n  \"fetch-policy\" : [ \"mgmt_172.23.26.39-jaguar_155_global1MGMT\" ],\n  \"advanced-settings\" : {\n    \"sam\" : {\n      \"forward-to-other-sam-servers\" : false,\n      \"purge-sam-file\" : {\n        \"enabled\" : false,\n        \"purge-when-size-reaches-to\" : 100\n      },\n      \"use-early-versions\" : {\n        \"enabled\" : false\n      }\n    },\n    \"connection-persistence\" : \"rematch-connections\"\n  },\n  \"enable-https-inspection\" : false,\n  \"https-inspection\" : {\n    \"bypass-on-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"site-categorization-allow-mode\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : \"hold\"\n    },\n    \"deny-untrusted-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"deny-expired-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"outbound-certificate\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : {\n        \"uid\" : \"f215045c-a773-45c2-8f71-0ff3e25c3b2d\",\n        \"name\" : \"OutboundCertificate\",\n        \"type\" : \"outbound-inspection-certificate\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"subject_user_certificate\",\n        \"color\" : \"black\"\n      }\n    },\n    \"deny-revoked-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    }\n  },\n  \"identity-awareness-settings\" : {\n    \"remote-access\" : false,\n    \"browser-based-authentication\" : false,\n    \"identity-agent\" : true,\n    \"identity-collector\" : false,\n    \"ad-query\" : false,\n    \"terminal-servers\" : false,\n    \"radius-accounting\" : false,\n    \"collecting-identities\" : false,\n    \"identity-agent-settings\" : {\n      \"agents-interval-keepalive\" : 5,\n      \"user-reauthenticate-interval\" : 480,\n      \"identity-agent-portal-settings\" : {\n        \"portal-web-settings\" : {\n          \"main-url\" : \"https://0.0.0.0/_IAAgent\",\n          \"ip-address\" : \"0.0.0.0\"\n        },\n        \"accessibility\" : {\n          \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n          \"internal-access-settings\" : {\n            \"undefined\" : false,\n            \"dmz\" : false,\n            \"vpn\" : false\n          }\n        }\n      },\n      \"authentication-settings\" : {\n        \"authentication-method\" : \"defined_on_user\",\n        \"users-directories\" : {\n          \"internal-users\" : false,\n          \"external-user-profile\" : false,\n          \"users-from-external-directories\" : \"all gateways directories\"\n        }\n      }\n    },\n    \"identity-sharing-settings\" : {\n      \"share-with-other-gateways\" : false,\n      \"receive-from-other-gateways\" : true,\n      \"cache-mode\" : {\n        \"override-profile\" : true,\n        \"profile-value\" : true,\n        \"value\" : true\n      },\n      \"cache-mode-duration\" : {\n        \"override-profile\" : true,\n        \"profile-value\" : 60,\n        \"value\" : 99\n      },\n      \"receive-from\" : [ {\n        \"uid\" : \"e141f65f-ba7e-40cd-913c-fb9e08b56504\",\n        \"name\" : \"IDServerGW\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      } ]\n    },\n    \"proxy-settings\" : {\n      \"detect-using-x-forward-for\" : false\n    },\n    \"identity-based-enforcement\" : \"on\",\n    \"identity-web-api\" : false\n  },\n  \"proxy-settings\" : {\n    \"use-custom-proxy\" : false\n  }\n}"
    },
    "add-simple-gateway with platform portal configuration": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"ipv4-address\" : \"1.1.1.1\",\n  \"platform-portal-settings\" : {\n    \"portal-web-settings\" : {\n      \"main-url\" : \"https://1.1.1.1/\",\n      \"ip-address\" : \"1.1.1.1\",\n      \"aliases\" : [ \"www.blabla1.com\" ]\n    },\n    \"certificate-settings\" : {\n      \"base64-certificate\" : \"MIIK4QIBAzCCCqcGCSqGSIb3DQEHAaCCCpgEggqUMIIKkDCCBUcGCSqGSIb3DQEHBqCCBTgwggU0AgEAMIIFLQYJKoZIhvcNAQcBMBwGCiqGSIb3DQEMAQYwDgQI0Ot32GaJy4kCAggAgIIFAPhJmOktQq5TCaDUSlQkwFVCLjhTNjc6q93xsTx+HIrbdnDNYMF7jc2PA5zA8gYzlb3jvL4hMUEQrkI/ot2MGxdy4lFRCwoXm7sUhkPbCPOF0URGVqwSHDHWnwe0kH08vlJBcWtJn72fkKkD7an5ElLeNyPn0PHghckrU8Q+/O3Y/nk+BuzPMdjnKWIZu1bAJs27CX9ISm3KwcMoVrHwfeqMbK9KxQ7zRy70RQgUqegrClbCADVcAAKpOABZNkoQri4wJVnXS7/N3nvHDohk1HVsewbdu6JGvx2gaOAg1ImXBsHuy1vmQBDH9oa0mZHb7Tp/bKqBbWuDHLPLEzrItzhijd+1dKrs3C6SZRcbmaNB9YQqQW3bKLGXbf0K2jGuoB4xGHrqmrjq5Ey/nK8pPLuoQ85UelY7bpwsk3H4fBiceHv4ZzDYPYFbdmnY5zI728MrM04YHB74DnYvGRo+7vcTt1RtUCABCKxLUJkuKNqg2qTVKJoK9534F+Je9LJT9EPyrW4v484kE4lENSHcJMJzxqx+fSTNkUloA/zyvAXlAwQjAsEhy13IrtCOmjGobPRLpcDkKDbsTRRsEZ2fxjLbdA5zKQIXWB1yebtIh0mSRwyxICZp9YGBjWRZ1Ukv4O1bLjzw7KZuY6QwSAN8RPmDwICoVcCJ02H3hTtfj5buT3c7KC+zEgwcvQixi0aMjMtoNKV+N846YTIAQKb0cr3uf4dOE1rgNeSyGHJ8YgOwkd4xk1ODEFkbbsHCnRqPSX9a4z3IChMnhoa2k3vThg267L0REATUTJ0lUzE9JXzKEVCXrKNhDs+jNmQ8L+laiMZEOPIMXfBjN6y1skF3dMLKSJcy0QqI+A4OgePQKaPzp2uLoQXMOHtDZ7XVSeRT0jNOqQMfxi/zMCl6ZDxpzaUjfpzxHlrKWfyehH43CGk7lYHFDePt6sh8k01q2uq8+2W29G4cmZfKK449RrqhoI9CiIzaVXPk72VVD/ReRrVIk6Avs2gZFpP1g7ai/+ynSeJyzVR3Fs3k81fPSmzoH5AuiZaru2WQO/5Dg5A6S6cDGLUTY4WhF1R5ffCO5O0JhtOFLxYvasI/0NnZFpsZflFcfBbGcwoqOmU2ztEWlPalfXTxyY8noq6UoH6nrDGD5p4wttj+kij2m5w0Baq5RqQxJHJwKaNthddJygbg074AVRM97ojHNxeh9xHgt3XOyDKADWg2A33XaHdDR219ZwZWuFxucb+0sZeKXyzd7ceUAcu/0Ouhv7HacBMzZkb9DQAasF6mDr3GagHfbPauH6qwbLKI+cDE30FM4rfJLW4hoZqASdotvLe1xs/RUmOfH9vsITK86ZZDVzzSBQmwaOPKA2m4WDb51P57820VeTcg2VtlwkHophaWjRpF3pzrYcX9RpHfa34biP943cSrq4U/2Eblxf6hUuvdl/4MdTnpBAbrxjdo9fJmdO+AnQ3x9IjAir58eu63vIMFKn/tEgUU1kDRELcOMYTinAy1Gp0U/0VdXJ5etGa/s1NC7p9gLII4zbhtLr7BMMTAgL33+nVK4OiEl+INmgqjlndG1WCT3J8KP9yv2NrHqlP/ymGvfnMwkjDLEEPv2gZcn6lkOKu/kZUgNOJH4bGeZwhG9dqoN6Z9YuMkLmC8o7PT/pLHBt7kxLezSvpD68H4rV+xZNQFOwyPO10nLXJlwOtIYVisMIIFQQYJKoZIhvcNAQcBoIIFMgSCBS4wggUqMIIFJgYLKoZIhvcNAQwKAQKgggTuMIIE6jAcBgoqhkiG9w0BDAEDMA4ECPxdMZc5K7NhAgIIAASCBMhwxZzl5X4cDxW+lpnvd6uWWOOs6AHJa8//QUZ9CAwVvcMuwaH8DPhFLQQnhY9KPJYsj8fG4Qsx8M+IN9Y+WHrYcDx/fL0aOmW1PunFonTeEJ/JaoKaNeLgVICHzN90Ph8Zz3B2X9JA9znnJkyX5l64OkLS0ZoEYN/aD9Lk+fFgx9vx17oseI5Kr49Usqa9EUuMWH0aFbKhwErOcz6Eh81khfCrIOLbsKTFi80LJR6ttS39kCzUWVoSbWGuEIOXnH6vGrm6PkXRZI2YZTvttnuThc/+k51jswnHVqvUi8I5amllsQWNGnIW2yzNg7ZNfEYkKEavyP4Tpuaa8PmQf579k+pO/mX6CLZRiBCb7L/tZ8YsM8+HTqGqJh31APgMRUwrTq4tgT1a6rNFx67hg2uys+QORdp+pK/r6pOOOw1U2vo0EG9viZM42j+6lH33yuH/QOnC63saZVVIUNnnoaqhOi1YT+LR/5PSWi9J7lf2AMAK66hQhFcTrZsvI8EfVKAzCSb0TamA58xGzHhT+lMqPJIrSc4QBWdfI4tqXSKAH0YvWkh9Btzhyy1ts4MqM8owm75J52a3DjqBi6bYN75QRL1mjs0Ua6AlCEMfT6Dqisefe5sQMZLnbceNfORAOLvd804UriEBzrONzXb240Y3+i527S/8tyjAWcPmmXZE5xO1H+fKsA1J3TC4eeV+6cPXybPVDVyVhPFkz5JpGYkxjAH3EAngW/EPSMsRHcxY3NqfNc/VO/i4h1ogYNKf/1GWXM00434ybdq+rMlpO/A3poJ06QDglEon3kr97KQkygOXd7MWS4xfiBWQP7dsqpmJZnXtMQ00iCOhaFrMG7AvsedTEoOFmhXvbf/ffd2tD/UAmm01fkyHfpJvi3gu/86NBVxM7eJDLZ1FLdqgNMBorln3R4yfqeb7NlssXo2lCMs5NYM2y7e5pt2BRvAYbcBpLaH+7B8Oiq/YXOkLgl+yLwFomnsD00XLYQ/WcNBCxOlc40DyUnxKplz1qGeMPIaZHiPkBiQ/MnA/aQ+wAdhV2gQxpY4aqiKtC/vFFbOnxuFlcnKKWKXkpu2khXsvSR598v+uip8FRW87Wrxtb/mYqmKnwcruIjzwm9O9XShC7XpmYWNtADfkddfuv+qF4tjGkimaw8zIF3smOGm60rjr2mm2NuKvf9Eez6lwxBtijsAixTd3OUpXQKq9UP2OU9h9cybxxb5Wctbe5UMVCSkSy+Om5sKh2x25MqKdbrjMbtDHOUS5IvHkdminkEyFKFsBi5o77cG8Sa14Ibu3Dq7eRjpNg0NOzTrE0HYdfB0TF8CgiUpXsgPeuXVwHAwkoWqNUxMgW8LTtaKEG22pOYF1BkzUcEeLMnfILQhDwmqUSgOneJ5JtEy+GPSqIJq2XCgSCnPr1C1ihzO2dWU+NfVkxo/qbN9+BSZuDCW30Vmkd3JKsVdANkYf/3kTp3F1K5Au/qgA9BchnHU5WKusFTO/yf8U68UBkufskOby4DsBxG9kZbygOre5SbzI+rdxZVYWgDafhylW/j9q/TlIQGdhQaOfhdiPunTRpZ0UECiyuLv2cUEC7NhTpj0grUyXn2i3DjvdED3K3FbSYJZ0NAJbG94RJSAqNswxJTAjBgkqhkiG9w0BCRUxFgQUKNireaeXb+7TbR3wuaw9Pza3xN8wMTAhMAkGBSsOAwIaBQAEFDFG6JpY3gFhgVF1JsyNo2D+zU5RBAg4bqQ33t/vZAICCAA=\",\n      \"base64-password\" : \"YmFkc3NsLmNvbQ==\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n      \"internal-access-settings\" : {\n        \"undefined\" : true,\n        \"dmz\" : true,\n        \"vpn\" : true\n      }\n    }\n  }\n}",
      "response": "{\n  \"uid\" : \"388b5d33-80f8-4059-9c91-8896d2aa99e8\",\n  \"name\" : \"gw1\",\n  \"type\" : \"simple-gateway\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1605796470032,\n      \"iso-8601\" : \"2020-11-19T16:34+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1605796470032,\n      \"iso-8601\" : \"2020-11-19T16:34+0200\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"1.1.1.1\",\n  \"dynamic-ip\" : false,\n  \"version\" : \"R81\",\n  \"os-name\" : \"Gaia\",\n  \"hardware\" : \"Open server\",\n  \"sic-name\" : \"\",\n  \"sic-state\" : \"uninitialized\",\n  \"interfaces\" : [ ],\n  \"firewall\" : true,\n  \"firewall-settings\" : {\n    \"auto-maximum-limit-for-concurrent-connections\" : true,\n    \"maximum-limit-for-concurrent-connections\" : 25000,\n    \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n    \"connections-hash-size\" : 131072,\n    \"memory-pool-size\" : 6,\n    \"maximum-memory-pool-size\" : 30\n  },\n  \"vpn\" : false,\n  \"application-control\" : false,\n  \"url-filtering\" : false,\n  \"content-awareness\" : false,\n  \"ips\" : false,\n  \"anti-bot\" : false,\n  \"anti-virus\" : false,\n  \"threat-emulation\" : false,\n  \"threat-extraction\" : false,\n  \"identity-awareness\" : false,\n  \"save-logs-locally\" : false,\n  \"send-alerts-to-server\" : [ \"ice-t392-mp-api-main-take-12\" ],\n  \"send-logs-to-server\" : [ \"ice-t392-mp-api-main-take-12\" ],\n  \"send-logs-to-backup-server\" : [ ],\n  \"logs-settings\" : {\n    \"rotate-log-by-file-size\" : false,\n    \"rotate-log-file-size-threshold\" : 1000,\n    \"rotate-log-on-schedule\" : false,\n    \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"alert-when-free-disk-space-below\" : true,\n    \"alert-when-free-disk-space-below-threshold\" : 20,\n    \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n    \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"delete-when-free-disk-space-below\" : true,\n    \"delete-when-free-disk-space-below-threshold\" : 5000,\n    \"before-delete-keep-logs-from-the-last-days\" : false,\n    \"before-delete-keep-logs-from-the-last-days-threshold\" : 3664,\n    \"before-delete-run-script\" : false,\n    \"before-delete-run-script-command\" : \"\",\n    \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"stop-logging-when-free-disk-space-below\" : true,\n    \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n    \"reject-connections-when-free-disk-space-below-threshold\" : false,\n    \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n    \"reserve-for-packet-capture-threshold\" : 500,\n    \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n    \"delete-index-files-when-index-size-above\" : false,\n    \"delete-index-files-when-index-size-above-threshold\" : 100000,\n    \"delete-index-files-older-than-days\" : false,\n    \"delete-index-files-older-than-days-threshold\" : 14,\n    \"forward-logs-to-log-server\" : false,\n    \"perform-log-rotate-before-log-forwarding\" : false,\n    \"update-account-log-every\" : 3600,\n    \"detect-new-citrix-ica-application-names\" : false,\n    \"turn-on-qos-logging\" : true\n  },\n  \"platform-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"main-url\" : \"https://1.1.1.1/\",\n      \"ip-address\" : \"1.1.1.1\",\n      \"aliases\" : [ \"www.blabla1.com\" ]\n    },\n    \"certificate-settings\" : {\n      \"certificate-valid-from\" : \"16-Nov-17\",\n      \"certificate-valid-to\" : \"16-Nov-19\",\n      \"certificate-dn\" : \"CN=BadSSL Client Certificate,O=BadSSL,L=San Francisco,ST=California,C=US\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n      \"internal-access-settings\" : {\n        \"undefined\" : true,\n        \"dmz\" : true,\n        \"vpn\" : true\n      }\n    }\n  },\n  \"enable-https-inspection\" : false,\n  \"https-inspection\" : {\n    \"bypass-on-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"site-categorization-allow-mode\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : \"hold\"\n    },\n    \"deny-untrusted-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"deny-expired-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"outbound-certificate\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : {\n        \"uid\" : \"f215045c-a773-45c2-8f71-0ff3e25c3b2d\",\n        \"name\" : \"OutboundCertificate\",\n        \"type\" : \"outbound-inspection-certificate\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"subject_user_certificate\",\n        \"color\" : \"black\"\n      }\n    },\n    \"deny-revoked-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    }\n  }\n}"
    },
    "add-simple-gateway with sic": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"color\" : \"yellow\",\n  \"ipv4-address\" : \"192.0.2.230\",\n  \"version\" : \"R80\",\n  \"one-time-password\" : \"aaaa\",\n  \"firewall\" : true,\n  \"vpn\" : true,\n  \"application-control\" : true,\n  \"url-filtering\" : true,\n  \"ips\" : true,\n  \"anti-bot\" : true,\n  \"anti-virus\" : true,\n  \"threat-emulation\" : true,\n  \"nat-hide-internal-interfaces\" : true,\n  \"icap-server\" : true,\n  \"interfaces\" : [ {\n    \"name\" : \"eth0\",\n    \"ipv4-address\" : \"192.0.2.230\",\n    \"ipv4-network-mask\" : \"255.255.255.128\",\n    \"anti-spoofing\" : true,\n    \"topology\" : \"EXTERNAL\"\n  }, {\n    \"name\" : \"eth1\",\n    \"ipv4-address\" : \"192.0.2.88\",\n    \"ipv4-network-mask\" : \"255.255.255.0\",\n    \"anti-spoofing\" : true,\n    \"topology\" : \"INTERNAL\"\n  } ]\n}",
      "response": ""
    },
    "add-simple-gateway with UserCheck portal configuration and with show-portals-certificate flag": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"ipv4-address\" : \"1.1.1.1\",\n  \"application-control\" : true,\n  \"usercheck-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"aliases\" : [ \"www.blabla1.com\" ]\n    },\n    \"certificate-settings\" : {\n      \"base64-certificate\" : \"MIIK4QIBAzCCCqcGCSqGSIb3DQEHAaCCCpgEggqUMIIKkDCCBUcGCSqGSIb3DQEHBqCCBTgwggU0AgEAMIIFLQYJKoZIhvcNAQcBMBwGCiqGSIb3DQEMAQYwDgQI0Ot32GaJy4kCAggAgIIFAPhJmOktQq5TCaDUSlQkwFVCLjhTNjc6q93xsTx+HIrbdnDNYMF7jc2PA5zA8gYzlb3jvL4hMUEQrkI/ot2MGxdy4lFRCwoXm7sUhkPbCPOF0URGVqwSHDHWnwe0kH08vlJBcWtJn72fkKkD7an5ElLeNyPn0PHghckrU8Q+/O3Y/nk+BuzPMdjnKWIZu1bAJs27CX9ISm3KwcMoVrHwfeqMbK9KxQ7zRy70RQgUqegrClbCADVcAAKpOABZNkoQri4wJVnXS7/N3nvHDohk1HVsewbdu6JGvx2gaOAg1ImXBsHuy1vmQBDH9oa0mZHb7Tp/bKqBbWuDHLPLEzrItzhijd+1dKrs3C6SZRcbmaNB9YQqQW3bKLGXbf0K2jGuoB4xGHrqmrjq5Ey/nK8pPLuoQ85UelY7bpwsk3H4fBiceHv4ZzDYPYFbdmnY5zI728MrM04YHB74DnYvGRo+7vcTt1RtUCABCKxLUJkuKNqg2qTVKJoK9534F+Je9LJT9EPyrW4v484kE4lENSHcJMJzxqx+fSTNkUloA/zyvAXlAwQjAsEhy13IrtCOmjGobPRLpcDkKDbsTRRsEZ2fxjLbdA5zKQIXWB1yebtIh0mSRwyxICZp9YGBjWRZ1Ukv4O1bLjzw7KZuY6QwSAN8RPmDwICoVcCJ02H3hTtfj5buT3c7KC+zEgwcvQixi0aMjMtoNKV+N846YTIAQKb0cr3uf4dOE1rgNeSyGHJ8YgOwkd4xk1ODEFkbbsHCnRqPSX9a4z3IChMnhoa2k3vThg267L0REATUTJ0lUzE9JXzKEVCXrKNhDs+jNmQ8L+laiMZEOPIMXfBjN6y1skF3dMLKSJcy0QqI+A4OgePQKaPzp2uLoQXMOHtDZ7XVSeRT0jNOqQMfxi/zMCl6ZDxpzaUjfpzxHlrKWfyehH43CGk7lYHFDePt6sh8k01q2uq8+2W29G4cmZfKK449RrqhoI9CiIzaVXPk72VVD/ReRrVIk6Avs2gZFpP1g7ai/+ynSeJyzVR3Fs3k81fPSmzoH5AuiZaru2WQO/5Dg5A6S6cDGLUTY4WhF1R5ffCO5O0JhtOFLxYvasI/0NnZFpsZflFcfBbGcwoqOmU2ztEWlPalfXTxyY8noq6UoH6nrDGD5p4wttj+kij2m5w0Baq5RqQxJHJwKaNthddJygbg074AVRM97ojHNxeh9xHgt3XOyDKADWg2A33XaHdDR219ZwZWuFxucb+0sZeKXyzd7ceUAcu/0Ouhv7HacBMzZkb9DQAasF6mDr3GagHfbPauH6qwbLKI+cDE30FM4rfJLW4hoZqASdotvLe1xs/RUmOfH9vsITK86ZZDVzzSBQmwaOPKA2m4WDb51P57820VeTcg2VtlwkHophaWjRpF3pzrYcX9RpHfa34biP943cSrq4U/2Eblxf6hUuvdl/4MdTnpBAbrxjdo9fJmdO+AnQ3x9IjAir58eu63vIMFKn/tEgUU1kDRELcOMYTinAy1Gp0U/0VdXJ5etGa/s1NC7p9gLII4zbhtLr7BMMTAgL33+nVK4OiEl+INmgqjlndG1WCT3J8KP9yv2NrHqlP/ymGvfnMwkjDLEEPv2gZcn6lkOKu/kZUgNOJH4bGeZwhG9dqoN6Z9YuMkLmC8o7PT/pLHBt7kxLezSvpD68H4rV+xZNQFOwyPO10nLXJlwOtIYVisMIIFQQYJKoZIhvcNAQcBoIIFMgSCBS4wggUqMIIFJgYLKoZIhvcNAQwKAQKgggTuMIIE6jAcBgoqhkiG9w0BDAEDMA4ECPxdMZc5K7NhAgIIAASCBMhwxZzl5X4cDxW+lpnvd6uWWOOs6AHJa8//QUZ9CAwVvcMuwaH8DPhFLQQnhY9KPJYsj8fG4Qsx8M+IN9Y+WHrYcDx/fL0aOmW1PunFonTeEJ/JaoKaNeLgVICHzN90Ph8Zz3B2X9JA9znnJkyX5l64OkLS0ZoEYN/aD9Lk+fFgx9vx17oseI5Kr49Usqa9EUuMWH0aFbKhwErOcz6Eh81khfCrIOLbsKTFi80LJR6ttS39kCzUWVoSbWGuEIOXnH6vGrm6PkXRZI2YZTvttnuThc/+k51jswnHVqvUi8I5amllsQWNGnIW2yzNg7ZNfEYkKEavyP4Tpuaa8PmQf579k+pO/mX6CLZRiBCb7L/tZ8YsM8+HTqGqJh31APgMRUwrTq4tgT1a6rNFx67hg2uys+QORdp+pK/r6pOOOw1U2vo0EG9viZM42j+6lH33yuH/QOnC63saZVVIUNnnoaqhOi1YT+LR/5PSWi9J7lf2AMAK66hQhFcTrZsvI8EfVKAzCSb0TamA58xGzHhT+lMqPJIrSc4QBWdfI4tqXSKAH0YvWkh9Btzhyy1ts4MqM8owm75J52a3DjqBi6bYN75QRL1mjs0Ua6AlCEMfT6Dqisefe5sQMZLnbceNfORAOLvd804UriEBzrONzXb240Y3+i527S/8tyjAWcPmmXZE5xO1H+fKsA1J3TC4eeV+6cPXybPVDVyVhPFkz5JpGYkxjAH3EAngW/EPSMsRHcxY3NqfNc/VO/i4h1ogYNKf/1GWXM00434ybdq+rMlpO/A3poJ06QDglEon3kr97KQkygOXd7MWS4xfiBWQP7dsqpmJZnXtMQ00iCOhaFrMG7AvsedTEoOFmhXvbf/ffd2tD/UAmm01fkyHfpJvi3gu/86NBVxM7eJDLZ1FLdqgNMBorln3R4yfqeb7NlssXo2lCMs5NYM2y7e5pt2BRvAYbcBpLaH+7B8Oiq/YXOkLgl+yLwFomnsD00XLYQ/WcNBCxOlc40DyUnxKplz1qGeMPIaZHiPkBiQ/MnA/aQ+wAdhV2gQxpY4aqiKtC/vFFbOnxuFlcnKKWKXkpu2khXsvSR598v+uip8FRW87Wrxtb/mYqmKnwcruIjzwm9O9XShC7XpmYWNtADfkddfuv+qF4tjGkimaw8zIF3smOGm60rjr2mm2NuKvf9Eez6lwxBtijsAixTd3OUpXQKq9UP2OU9h9cybxxb5Wctbe5UMVCSkSy+Om5sKh2x25MqKdbrjMbtDHOUS5IvHkdminkEyFKFsBi5o77cG8Sa14Ibu3Dq7eRjpNg0NOzTrE0HYdfB0TF8CgiUpXsgPeuXVwHAwkoWqNUxMgW8LTtaKEG22pOYF1BkzUcEeLMnfILQhDwmqUSgOneJ5JtEy+GPSqIJq2XCgSCnPr1C1ihzO2dWU+NfVkxo/qbN9+BSZuDCW30Vmkd3JKsVdANkYf/3kTp3F1K5Au/qgA9BchnHU5WKusFTO/yf8U68UBkufskOby4DsBxG9kZbygOre5SbzI+rdxZVYWgDafhylW/j9q/TlIQGdhQaOfhdiPunTRpZ0UECiyuLv2cUEC7NhTpj0grUyXn2i3DjvdED3K3FbSYJZ0NAJbG94RJSAqNswxJTAjBgkqhkiG9w0BCRUxFgQUKNireaeXb+7TbR3wuaw9Pza3xN8wMTAhMAkGBSsOAwIaBQAEFDFG6JpY3gFhgVF1JsyNo2D+zU5RBAg4bqQ33t/vZAICCAA=\",\n      \"base64-password\" : \"YmFkc3NsLmNvbQ==\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n      \"internal-access-settings\" : {\n        \"undefined\" : true,\n        \"dmz\" : true,\n        \"vpn\" : true\n      }\n    }\n  },\n  \"show-portals-certificate\" : true\n}",
      "response": "{\n  \"uid\" : \"42d0a54c-5fc0-471f-80f2-295cc3266967\",\n  \"name\" : \"gw1\",\n  \"type\" : \"simple-gateway\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1605800886308,\n      \"iso-8601\" : \"2020-11-19T17:48+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1605800883907,\n      \"iso-8601\" : \"2020-11-19T17:48+0200\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"1.1.1.1\",\n  \"dynamic-ip\" : false,\n  \"version\" : \"R81\",\n  \"os-name\" : \"Gaia\",\n  \"hardware\" : \"Open server\",\n  \"sic-name\" : \"\",\n  \"sic-state\" : \"uninitialized\",\n  \"interfaces\" : [ ],\n  \"firewall\" : true,\n  \"firewall-settings\" : {\n    \"auto-maximum-limit-for-concurrent-connections\" : true,\n    \"maximum-limit-for-concurrent-connections\" : 25000,\n    \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n    \"connections-hash-size\" : 131072,\n    \"memory-pool-size\" : 6,\n    \"maximum-memory-pool-size\" : 30\n  },\n  \"vpn\" : false,\n  \"application-control\" : true,\n  \"url-filtering\" : false,\n  \"content-awareness\" : false,\n  \"ips\" : false,\n  \"anti-bot\" : false,\n  \"anti-virus\" : false,\n  \"threat-emulation\" : false,\n  \"threat-extraction\" : false,\n  \"identity-awareness\" : false,\n  \"save-logs-locally\" : false,\n  \"send-alerts-to-server\" : [ \"ice-t392-mp-api-main-take-13\" ],\n  \"send-logs-to-server\" : [ \"ice-t392-mp-api-main-take-13\" ],\n  \"send-logs-to-backup-server\" : [ ],\n  \"logs-settings\" : {\n    \"rotate-log-by-file-size\" : false,\n    \"rotate-log-file-size-threshold\" : 1000,\n    \"rotate-log-on-schedule\" : false,\n    \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"alert-when-free-disk-space-below\" : true,\n    \"alert-when-free-disk-space-below-threshold\" : 20,\n    \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n    \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"delete-when-free-disk-space-below\" : true,\n    \"delete-when-free-disk-space-below-threshold\" : 5000,\n    \"before-delete-keep-logs-from-the-last-days\" : false,\n    \"before-delete-keep-logs-from-the-last-days-threshold\" : 3664,\n    \"before-delete-run-script\" : false,\n    \"before-delete-run-script-command\" : \"\",\n    \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"stop-logging-when-free-disk-space-below\" : true,\n    \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n    \"reject-connections-when-free-disk-space-below-threshold\" : false,\n    \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n    \"reserve-for-packet-capture-threshold\" : 500,\n    \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n    \"delete-index-files-when-index-size-above\" : false,\n    \"delete-index-files-when-index-size-above-threshold\" : 100000,\n    \"delete-index-files-older-than-days\" : false,\n    \"delete-index-files-older-than-days-threshold\" : 14,\n    \"forward-logs-to-log-server\" : false,\n    \"perform-log-rotate-before-log-forwarding\" : false,\n    \"update-account-log-every\" : 3600,\n    \"detect-new-citrix-ica-application-names\" : false,\n    \"turn-on-qos-logging\" : true\n  },\n  \"platform-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"main-url\" : \"https://1.1.1.1/\",\n      \"ip-address\" : \"1.1.1.1\"\n    },\n    \"certificate-settings\" : {\n      \"certificate-valid-from\" : \"16-Nov-17\",\n      \"certificate-valid-to\" : \"16-Nov-19\",\n      \"certificate-dn\" : \"CN=BadSSL Client Certificate,O=BadSSL,L=San Francisco,ST=California,C=US\",\n      \"certificate\" : \"-----BEGIN CERTIFICATE-----MIIEnTCCAoWgAwIBAgIJAPC7KMFjfslXMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlhMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMQ8wDQYDVQQKDAZCYWRTU0wxMTAvBgNVBAMMKEJhZFNTTCBDbGllbnQgUm9vdCBDZXJ0aWZpY2F0ZSBBdXRob3JpdHkwHhcNMTcxMTE2MDUzNjMzWhcNMTkxMTE2MDUzNjMzWjBvMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEPMA0GA1UECgwGQmFkU1NMMSIwIAYDVQQDDBlCYWRTU0wgQ2xpZW50IENlcnRpZmljYXRlMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxzdfEeseTs/rukjly6MSLHM+Rh0enA3Ai4Mj2sdl31x3SbPoen08utVhjPmlxIUdkiMG4+ffe7N+JtDLG75CaxZp9CxytX7kywooRBJsRnQhmQPca8MRWAJBIz+w/L+3AFkTIqWBfyT+1VO8TVKPkEpGdLDovZOmzZAASi9/sj+j6gM7AaCiDeZTf2ES66abA5pOp60Q6OEdwg/vCUJfarhKDpi9tj3P6qToy9Y4DiBUhOct4MG8w5XwmKAC+Vfm8tb7tMiUoU0yvKKOcL6YXBXxB2kPcOYxYNobXavfVBEdwSrjQ7i/s3o6hkGQlm9F7JPEuVgbl/Jdwa64OYIqjQIDAQABoy0wKzAJBgNVHRMEAjAAMBEGCWCGSAGG+EIBAQQEAwIHgDALBgNVHQ8EBAMCBeAwDQYJKoZIhvcNAQELBQADggIBAKpzk1ZTunWuof3DIer2Abq7IV3STGeFaoH4TuHdSbmXwC0KuPkv7wVPgPekyRaHb9CBnsreRF7eleD1M63kakhdnA1XIbdJw8sfSDlKdI4emmb4fzdaaPxbrkQ5IxOBQDw5rTUFVPPqFWw1bGP2zrKD1/i1pxUtGM0xem1jR7UZYpsSPs0JCOHKZOmk8OEWUy+Jp4gRzbMLZ0TrvajGEZXRepjOkXObR81xZGtvTNP2wl1zm13ffwIYdqJUrf1HH4miU9lVX+3/Z+2mVHBWhzBgbTmo06s3uwUE6JsxUGm2/w4NNblRit0uQcGw7ba8kl2d5rZQscFsqNFz2vRjj1G0dO8S3owmuF0izZO9Fqvq0jB6oaUkxcAcTKFSjs2zwy1oy+cu8iO3GRbfAW7U0xzGp9MnkdPS5dHzvhod3/DK0YVskfxZF7M8GhkjT7Qm2EUBQNNMNXC3g/GXTdXOgqqjW5GXahI8Z6Q4OYN6xZwuEhizwKkgojwaww2YgYT9MJXciJZWr3QXvFdBH7m0zwpKgQ1wm6j3yeyuRphq2lEtU3OQl55A3tXtvqyMXsxkxMCCNQdmKQt0WYmMS3Xj/AfAY2sjCWziDflvW5mGCUjSYdZ+r3JIIF4m/FNCIO1dIoacp9qb0qL9duFlVHtFiPgoKrEdJaNVUL7NG9ppF8pR-----END CERTIFICATE-----\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"RULE_BASE\"\n    }\n  },\n  \"usercheck-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"main-url\" : \"http://1.1.1.1/UserCheck\",\n      \"ip-address\" : \"1.1.1.1\",\n      \"aliases\" : [ \"www.blabla1.com\" ]\n    },\n    \"certificate-settings\" : {\n      \"certificate-valid-from\" : \"16-Nov-17\",\n      \"certificate-valid-to\" : \"16-Nov-19\",\n      \"certificate-dn\" : \"CN=BadSSL Client Certificate,O=BadSSL,L=San Francisco,ST=California,C=US\",\n      \"certificate\" : \"-----BEGIN CERTIFICATE-----MIIEnTCCAoWgAwIBAgIJAPC7KMFjfslXMA0GCSqGSIb3DQEBCwUAMH4xCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlhMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMQ8wDQYDVQQKDAZCYWRTU0wxMTAvBgNVBAMMKEJhZFNTTCBDbGllbnQgUm9vdCBDZXJ0aWZpY2F0ZSBBdXRob3JpdHkwHhcNMTcxMTE2MDUzNjMzWhcNMTkxMTE2MDUzNjMzWjBvMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEPMA0GA1UECgwGQmFkU1NMMSIwIAYDVQQDDBlCYWRTU0wgQ2xpZW50IENlcnRpZmljYXRlMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAxzdfEeseTs/rukjly6MSLHM+Rh0enA3Ai4Mj2sdl31x3SbPoen08utVhjPmlxIUdkiMG4+ffe7N+JtDLG75CaxZp9CxytX7kywooRBJsRnQhmQPca8MRWAJBIz+w/L+3AFkTIqWBfyT+1VO8TVKPkEpGdLDovZOmzZAASi9/sj+j6gM7AaCiDeZTf2ES66abA5pOp60Q6OEdwg/vCUJfarhKDpi9tj3P6qToy9Y4DiBUhOct4MG8w5XwmKAC+Vfm8tb7tMiUoU0yvKKOcL6YXBXxB2kPcOYxYNobXavfVBEdwSrjQ7i/s3o6hkGQlm9F7JPEuVgbl/Jdwa64OYIqjQIDAQABoy0wKzAJBgNVHRMEAjAAMBEGCWCGSAGG+EIBAQQEAwIHgDALBgNVHQ8EBAMCBeAwDQYJKoZIhvcNAQELBQADggIBAKpzk1ZTunWuof3DIer2Abq7IV3STGeFaoH4TuHdSbmXwC0KuPkv7wVPgPekyRaHb9CBnsreRF7eleD1M63kakhdnA1XIbdJw8sfSDlKdI4emmb4fzdaaPxbrkQ5IxOBQDw5rTUFVPPqFWw1bGP2zrKD1/i1pxUtGM0xem1jR7UZYpsSPs0JCOHKZOmk8OEWUy+Jp4gRzbMLZ0TrvajGEZXRepjOkXObR81xZGtvTNP2wl1zm13ffwIYdqJUrf1HH4miU9lVX+3/Z+2mVHBWhzBgbTmo06s3uwUE6JsxUGm2/w4NNblRit0uQcGw7ba8kl2d5rZQscFsqNFz2vRjj1G0dO8S3owmuF0izZO9Fqvq0jB6oaUkxcAcTKFSjs2zwy1oy+cu8iO3GRbfAW7U0xzGp9MnkdPS5dHzvhod3/DK0YVskfxZF7M8GhkjT7Qm2EUBQNNMNXC3g/GXTdXOgqqjW5GXahI8Z6Q4OYN6xZwuEhizwKkgojwaww2YgYT9MJXciJZWr3QXvFdBH7m0zwpKgQ1wm6j3yeyuRphq2lEtU3OQl55A3tXtvqyMXsxkxMCCNQdmKQt0WYmMS3Xj/AfAY2sjCWziDflvW5mGCUjSYdZ+r3JIIF4m/FNCIO1dIoacp9qb0qL9duFlVHtFiPgoKrEdJaNVUL7NG9ppF8pR-----END CERTIFICATE-----\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"INTERNAL_INTERFACES\",\n      \"internal-access-settings\" : {\n        \"undefined\" : true,\n        \"dmz\" : true,\n        \"vpn\" : true\n      }\n    }\n  },\n  \"enable-https-inspection\" : false,\n  \"https-inspection\" : {\n    \"bypass-on-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"site-categorization-allow-mode\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : \"hold\"\n    },\n    \"deny-untrusted-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"deny-expired-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"outbound-certificate\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : {\n        \"uid\" : \"f215045c-a773-45c2-8f71-0ff3e25c3b2d\",\n        \"name\" : \"OutboundCertificate\",\n        \"type\" : \"outbound-inspection-certificate\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"subject_user_certificate\",\n        \"color\" : \"black\"\n      }\n    },\n    \"deny-revoked-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    }\n  }\n}"
    },
    "add-simple-gateway with vpn certificate": {
      "description": "",
      "request": "POST {{server}}/add-simple-gateway\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"gw1\",\n  \"ip-address\" : \"1.1.1.1\",\n  \"vpn-settings\" : {\n    \"certificates\" : {\n      \"name\" : \"new_cert\",\n      \"certificate-authority\" : \"trusted_ca\",\n      \"enrollment\" : {\n        \"enrollment-settings\" : {\n          \"distinguished-name\" : \"CN=test\"\n        }\n      }\n    }\n  }\n}",
      "response": "{\n  \"uid\" : \"212b5cf1-be85-483a-8eed-cfcddbac9c94\",\n  \"name\" : \"gw1\",\n  \"type\" : \"simple-gateway\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"platform\" : \"open server\",\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1708605674325,\n      \"iso-8601\" : \"2024-02-22T14:41+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1708605674325,\n      \"iso-8601\" : \"2024-02-22T14:41+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"available-actions\" : {\n    \"clone\" : \"not_supported\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"nat-settings\" : {\n    \"auto-rule\" : false\n  },\n  \"ipv4-address\" : \"1.1.1.1\",\n  \"dynamic-ip\" : false,\n  \"version\" : \"R82\",\n  \"os-name\" : \"Gaia\",\n  \"hardware\" : \"Open server\",\n  \"interfaces\" : [ ],\n  \"network-policy-management\" : false,\n  \"log-server\" : false,\n  \"firewall\" : true,\n  \"firewall-settings\" : {\n    \"auto-maximum-limit-for-concurrent-connections\" : true,\n    \"maximum-limit-for-concurrent-connections\" : 25000,\n    \"auto-calculate-connections-hash-table-size-and-memory-pool\" : true,\n    \"connections-hash-size\" : 131072,\n    \"memory-pool-size\" : 6,\n    \"maximum-memory-pool-size\" : 30\n  },\n  \"vpn\" : true,\n  \"vpn-settings\" : {\n    \"useClientlessVpn\" : false,\n    \"maximum-concurrent-ike-negotiations\" : 10000,\n    \"maximum-concurrent-tunnels\" : 10000,\n    \"vpn-domain-type\" : \"addresses_behind_gw\",\n    \"link-selection\" : {\n      \"ip-selection\" : \"use-main-address\"\n    },\n    \"remote-access\" : {\n      \"support-l2tp\" : false,\n      \"allow-vpn-clients-to-route-traffic\" : false,\n      \"support-nat-traversal-mechanism\" : true,\n      \"nat-traversal-service\" : {\n        \"uid\" : \"97aeb390-9aea-11d5-bd16-0090272ccb30\",\n        \"name\" : \"VPN1_IPSEC_encapsulation\",\n        \"type\" : \"service-udp\",\n        \"domain\" : {\n          \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n          \"name\" : \"Check Point Data\",\n          \"domain-type\" : \"data domain\"\n        },\n        \"icon\" : \"Services/UDPService\",\n        \"color\" : \"firebrick\",\n        \"port\" : \"2746\"\n      },\n      \"support-visitor-mode\" : true,\n      \"visitor-mode-service\" : {\n        \"uid\" : \"97aeb443-9aea-11d5-bd16-0090272ccb30\",\n        \"name\" : \"https\",\n        \"type\" : \"service-tcp\",\n        \"domain\" : {\n          \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n          \"name\" : \"Check Point Data\",\n          \"domain-type\" : \"data domain\"\n        },\n        \"icon\" : \"Protocols/HTTP\",\n        \"color\" : \"red\",\n        \"port\" : \"443\"\n      },\n      \"visitor-mode-interface\" : \"All IPs\"\n    },\n    \"office-mode\" : {\n      \"mode\" : \"off\"\n    },\n    \"vpn-domain-exclude-external-ip-addresses\" : false,\n    \"interfaces\" : [ ],\n    \"certificates\" : [ {\n      \"name\" : \"new_cert\",\n      \"type\" : \"CpmiCertificate\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"distinguished-name\" : \"CN=test\",\n      \"certificate-authority\" : {\n        \"uid\" : \"c311ebd0-dbe9-4e84-b26b-85e7a1913e08\",\n        \"name\" : \"trusted_ca\",\n        \"type\" : \"opsec-trusted-ca\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"Objects/account_unit\",\n        \"color\" : \"black\"\n      },\n      \"status\" : \"unsigned\",\n      \"stored-at\" : \"management server\",\n      \"base64-certificate\" : \"-----BEGIN CERTIFICATE REQUEST-----\\nMIICcjCCAVoCAQAwDzENMAsGA1UEAxMEdGVzdDCCASIwDQYJKoZIhvcNAQEBBQAD\\r\\nggEPADCCAQoCggEBAKRDabAQDL6vAeX3zQqOQBdaMZEn06pxY5yx2B6shCYXdc8F\\r\\nITkaTGFxNCimin1A+lW0AB5pIh+aVsBW4PCmU0sklzMnS2NudznKc27Zpwq9OK9c\\r\\nuUCw6rmRyTv5otdViP2lmfP50PPA8+b3lefHbXecwKSJ8l9MH/sl+XYViaYRVJUO\\r\\n1oFOh0mT9f/of0gx8PjbnFVGIxStZEcY/gqhETk7EV3msd+6CLhPKbDt8wq6IIPo\\r\\nF9yHc9T6EGWN7KEgxFik/9ObiAPUrqr37muVya5p7kLALwRSWcjOgmxXlbf1fQX1\\r\\nko40iDkmjpKKJx0NkXg+5Z2Ddz0JYk5Oo/hhhUUCAwEAAaAeMBwGCSqGSIb3DQEJ\\r\\nDjEPMA0wCwYDVR0PBAQDAgWgMA0GCSqGSIb3DQEBCwUAA4IBAQAVZeLbsILDoDrF\\r\\nW9yOc7uO5nQcwENBENU+u6PaeL7KPkCQCrZ4zV2f1WggZsQwBrN73Dw/bOaN1iuN\\r\\nzXUC6l2imsPeKH1ZO0fbgNPNNOiGYdJgSKmRW/Q3KcxPOvR3tHXHYsCBYE88oRLR\\r\\ncCUNQ/nLhkWQu8tc7kS65ynnxaYous8pusq0KpQC8BEzfpQQKlW2D7OFZLczKUeY\\r\\nhwm6F149Pl5+jvSJKOTeFOvEB02LFCv6Xd+W+kFwVrpIVZeOQ1vEB4qxnsqM8CjY\\r\\n40VO+peaLu0bsIxjkea9u2bmz+pPtIbXgIU+gXaQ8vi1X4Ikh8usiSJl1gxf0eak\\r\\nu2N/1PvR\\r\\n-----END CERTIFICATE REQUEST-----\"\n    }, {\n      \"name\" : \"defaultCert\",\n      \"type\" : \"CpmiCertificate\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"distinguished-name\" : \"CN=gw1 VPN Certificate,O=jaguar-t511-trusted-ca-main-take-3.checkpoint.com.877tdv\",\n      \"certificate-authority\" : {\n        \"uid\" : \"3fbbc166-4e00-7645-b802-0746485b6692\",\n        \"name\" : \"internal_ca\",\n        \"type\" : \"internal-trusted-ca\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"Objects/account_unit\",\n        \"color\" : \"black\"\n      },\n      \"status\" : \"signed\",\n      \"stored-at\" : \"management server\",\n      \"expiration-date\" : {\n        \"posix\" : 1740141673000,\n        \"iso-8601\" : \"2025-02-21T14:41+0200\"\n      },\n      \"base64-certificate\" : \"-----BEGIN CERTIFICATE-----\\nMIIEETCCAvmgAwIBAgICNBUwDQYJKoZIhvcNAQELBQAwQzFBMD8GA1UEChM4amFn\\r\\ndWFyLXQ1MTEtdHJ1c3RlZC1jYS1tYWluLXRha2UtMy5jaGVja3BvaW50LmNvbS44\\r\\nNzd0ZHYwHhcNMjQwMjIxMTI0MTEzWhcNMjUwMjIxMTI0MTEzWjBhMUEwPwYDVQQK\\r\\nEzhqYWd1YXItdDUxMS10cnVzdGVkLWNhLW1haW4tdGFrZS0zLmNoZWNrcG9pbnQu\\r\\nY29tLjg3N3RkdjEcMBoGA1UEAxMTZ3cxIFZQTiBDZXJ0aWZpY2F0ZTCCASIwDQYJ\\r\\nKoZIhvcNAQEBBQADggEPADCCAQoCggEBAL4svb8NPa9iVNhnS83oKhVRRGG8A053\\r\\niySmmGDIWJl3seMZnmJEehvkpPMlf00kbj7KyzKTyRjnKAJW9Jp35thU4P/5yQ9f\\r\\n7DvOtEC5coHmDb+Th7BnqFcVIvCfM/05GwdN4QvZ2WxmlAYV6x6rUnyA94EDrg8S\\r\\nAr1tcKMLjsXfeyRYBSyEqoT9wbc5gxKvKA1FmHngWLE8ApvytvtcJ7KbABKYwLas\\r\\nzOQODkGqkIGZ/lfraysZdfmsMaSg0PdIQbNVqv6QfIvkDU0BVDiv9xBbBbBBaKyz\\r\\n2Vjvc5RFS0k5nGIznTTV6rwKR7drMEC0nDWF7XeNshpPim868QUfvdUCAwEAAaOB\\r\\n8DCB7TCBrAYDVR0fBIGkMIGhMIGeoIGboIGYhjxodHRwOi8vamFndWFyLXQ1MTEt\\r\\ndHJ1c3RlZC1jYS1tYWluLXRha2UtMzoxODI2NC9JQ0FfQ1JMMS5jcmykWDBWMUEw\\r\\nPwYDVQQKEzhqYWd1YXItdDUxMS10cnVzdGVkLWNhLW1haW4tdGFrZS0zLmNoZWNr\\r\\ncG9pbnQuY29tLjg3N3RkdjERMA8GA1UEAwwISUNBX0NSTDEwCQYDVR0TBAIwADAP\\r\\nBgNVHREECDAGhwQBAQEBMAsGA1UdDwQEAwIFoDATBgNVHSUEDDAKBggrBgEFBQcD\\r\\nATANBgkqhkiG9w0BAQsFAAOCAQEAly5nG6O9KoyChj7F+EsSywm4jwl0dcPAUrmt\\r\\nmM0uSQI9k72J2y72OUf4ZQgEsbLFJ63AOSFBXylBDrzLE0gWd8xGHyPdoLGcjTgK\\r\\nZf7cLIszkz25nRJLxiFFEdr3vf4a7eiWr5a7+bI7GqwwJbnkukv8HjNF0nBUgPeX\\r\\nLAVqiWQqIVoKVJYuEEaTk+BY7SMT/Y9LgPvQDbhdNIgC8xc4S7/s+Mzlmp97hWTY\\r\\nhsXBM3cP3por0ZHyeBI/LYDgJuC8MmcX/DkKkWucNmdaCZY3ep/O9ji/dzVtdufD\\r\\nerP5FBCy6G6Jk/lB+EaYkULlE4ubxPHVOylE1sN0rlrsWJrlMg==\\r\\n-----END CERTIFICATE-----\\n\"\n    } ]\n  },\n  \"policy-server\" : false,\n  \"mobile-access\" : false,\n  \"application-control\" : false,\n  \"url-filtering\" : false,\n  \"legacy-url-filtering\" : false,\n  \"application-control-and-url-filtering-settings\" : {\n    \"global-settings-mode\" : \"use_global_settings\"\n  },\n  \"content-awareness\" : false,\n  \"monitoring\" : false,\n  \"rtm-traffic-report-per-connection\" : false,\n  \"rtm-traffic-report\" : false,\n  \"rtm-counters-report\" : true,\n  \"anti-spam-and-email-security\" : false,\n  \"threat-prevention-mode\" : \"custom\",\n  \"ips\" : false,\n  \"anti-bot\" : false,\n  \"anti-virus\" : false,\n  \"threat-emulation\" : false,\n  \"threat-extraction\" : false,\n  \"zero-phishing\" : false,\n  \"ips-update-policy\" : \"gateway automatic update\",\n  \"identity-awareness\" : false,\n  \"data-loss-prevention\" : false,\n  \"qos\" : false,\n  \"externally-managed\" : false,\n  \"hit-count\" : true,\n  \"sic-name\" : \"\",\n  \"sic-state\" : \"uninitialized\",\n  \"trust-state\" : \"uninitialized\",\n  \"save-logs-locally\" : false,\n  \"send-alerts-to-server\" : [ \"jaguar-t511-trusted-ca-main-take-3\" ],\n  \"send-logs-to-server\" : [ \"jaguar-t511-trusted-ca-main-take-3\" ],\n  \"send-logs-to-backup-server\" : [ ],\n  \"logs-settings\" : {\n    \"rotate-log-by-file-size\" : false,\n    \"rotate-log-file-size-threshold\" : 1000,\n    \"rotate-log-on-schedule\" : false,\n    \"alert-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"alert-when-free-disk-space-below\" : true,\n    \"alert-when-free-disk-space-below-threshold\" : 3000,\n    \"alert-when-free-disk-space-below-type\" : \"popup alert\",\n    \"delete-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"delete-when-free-disk-space-below\" : true,\n    \"delete-when-free-disk-space-below-threshold\" : 5000,\n    \"before-delete-keep-logs-from-the-last-days\" : false,\n    \"before-delete-keep-logs-from-the-last-days-threshold\" : 3664,\n    \"before-delete-run-script\" : false,\n    \"before-delete-run-script-command\" : \"\",\n    \"stop-logging-when-free-disk-space-below-metrics\" : \"mbytes\",\n    \"stop-logging-when-free-disk-space-below\" : true,\n    \"stop-logging-when-free-disk-space-below-threshold\" : 100,\n    \"reject-connections-when-free-disk-space-below-threshold\" : false,\n    \"reserve-for-packet-capture-metrics\" : \"mbytes\",\n    \"reserve-for-packet-capture-threshold\" : 500,\n    \"delete-index-files-when-index-size-above-metrics\" : \"mbytes\",\n    \"delete-index-files-when-index-size-above\" : false,\n    \"delete-index-files-when-index-size-above-threshold\" : 100000,\n    \"delete-index-files-older-than-days\" : false,\n    \"delete-index-files-older-than-days-threshold\" : 14,\n    \"forward-logs-to-log-server\" : false,\n    \"perform-log-rotate-before-log-forwarding\" : false,\n    \"update-account-log-every\" : 3600,\n    \"detect-new-citrix-ica-application-names\" : false,\n    \"turn-on-qos-logging\" : true,\n    \"distribute-logs-between-all-active-servers\" : false\n  },\n  \"platform-portal-settings\" : {\n    \"enabled\" : true,\n    \"portal-web-settings\" : {\n      \"main-url\" : \"https://1.1.1.1/\",\n      \"ip-address\" : \"1.1.1.1\"\n    },\n    \"accessibility\" : {\n      \"allow-access-from\" : \"RULE_BASE\"\n    }\n  },\n  \"nat-hide-internal-interfaces\" : false,\n  \"communication-with-servers-behind-nat\" : {\n    \"override-profile\" : false\n  },\n  \"fetch-policy\" : [ \"jaguar-t511-trusted-ca-main-take-3\" ],\n  \"advanced-settings\" : {\n    \"sam\" : {\n      \"forward-to-other-sam-servers\" : false,\n      \"purge-sam-file\" : {\n        \"enabled\" : false,\n        \"purge-when-size-reaches-to\" : 100\n      },\n      \"use-early-versions\" : {\n        \"enabled\" : false\n      }\n    },\n    \"connection-persistence\" : \"rematch-connections\"\n  },\n  \"enable-https-inspection\" : false,\n  \"https-inspection\" : {\n    \"bypass-on-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"site-categorization-allow-mode\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : \"hold\"\n    },\n    \"deny-untrusted-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"deny-expired-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : false\n    },\n    \"bypass-on-client-failure\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    },\n    \"bypass-under-load\" : {\n      \"value\" : false\n    },\n    \"deployment-mode\" : \"full\",\n    \"deny-revoked-server-cert\" : {\n      \"override-profile\" : false,\n      \"profile-value\" : true\n    }\n  },\n  \"zero-phishing-settings\" : {\n    \"gateway-fqdn-mode\" : \"automatic\"\n  },\n  \"auto-topology-use-custom-recalculation-time\" : false,\n  \"auto-topology-custom-recalculation-time\" : 10,\n  \"proxy-settings\" : {\n    \"use-custom-proxy\" : false\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:09.431026",
    "source_file": "add-simple-gateway.html"
  }
}
```