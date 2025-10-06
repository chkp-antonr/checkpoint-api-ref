# add-simple-cluster

```json
{
  "command": "add-simple-cluster",
  "description": "Create new object.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-simple-cluster",
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
        "name": "cluster-mode",
        "description": "Cluster mode.",
        "type": "string",
        "required": false,
        "default": "cluster-xl-ha",
        "valid_values": [
          "cluster-xl-ha",
          "cluster-ls-multicast",
          "cluster-ls-unicast",
          "opsec-ha",
          "opsec-ls"
        ]
      },
      {
        "name": "cluster-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "maintain-current-active",
        "valid_values": [
          "maintain-current-active",
          "according-to-priority"
        ]
      },
      {
        "name": "member-recovery-mode",
        "description": "In a High Availability cluster, each member is given a priority. The member with the highest priority serves as the gateway. If this gateway fails, control is passed to the member with the next highest priority. If that member fails, control is passed to the next, and so on. Upon gateway recovery, it is possible to: Maintain current active Cluster Member (maintain-current-active) or Switch to higher priority Cluster Member (according-to-priority).",
        "type": "string",
        "required": false,
        "default": "maintain-current-active",
        "valid_values": [
          "maintain-current-active",
          "according-to-priority"
        ]
      },
      {
        "name": "state-synchronization",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "delayed",
        "description": "Start synchronizing with delay of seconds, as defined by delayed-seconds, after connection initiation. Disabled when state-synchronization disabled.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "delayed-seconds",
        "description": "Start synchronizing X seconds after connection initiation . The values must be in a range between 2 and 3600.",
        "type": "integer",
        "required": false,
        "default": "3 seconds"
      },
      {
        "name": "enabled",
        "description": "Use State Synchronization.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "track-changes-of-cluster-members",
        "description": "Track changes in the status of Cluster Members.",
        "type": "string",
        "required": false,
        "default": "log",
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
        "name": "use-virtual-mac",
        "description": "Use Virtual MAC. By enabling Virtual MAC in ClusterXL High Availability New mode, or Load Sharing Unicast mode, all cluster members associate the same Virtual MAC address with All Cluster Virtual Interfaces and the Virtual IP address.",
        "type": "boolean",
        "required": false,
        "default": "false"
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
        "name": "geo-mode",
        "description": "Cluster High Availability Geo mode.This setting applies only to a cluster deployed in a cloud. Available when the cluster mode equals \"cluster-xl-ha\".",
        "type": "boolean",
        "required": false
      },
      {
        "name": "hardware",
        "description": "Cluster platform hardware.",
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
        "default": "prevent",
        "valid_values": [
          "cluster",
          "sync",
          "cluster + sync",
          "private"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "interface-type",
        "description": "Cluster interface type.",
        "type": "string",
        "required": true,
        "valid_values": [
          "cluster",
          "sync",
          "cluster + sync",
          "private"
        ]
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
        "required": false
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
        "name": "multicast-address",
        "description": "Multicast IP Address.",
        "type": "string",
        "required": false
      },
      {
        "name": "multicast-address-type",
        "description": "Multicast Address Type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "default"
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
        "name": "topology",
        "description": "N/A",
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
        "name": "reject-on-cluster-fail-over",
        "description": "Define the IPS connections during fail over reject packets or accept packets.",
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
        "name": "members",
        "description": "",
        "type": "array",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "auto-generate-ip",
        "description": "Use an automatically generated IP address for the Gateway object (applies only to Smart-1 Cloud).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "interfaces",
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
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
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
        "name": "topology",
        "description": "N/A",
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
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
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
        "name": "topology",
        "description": "N/A",
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "one-time-password",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "trust-method",
        "description": "Trust method to use for establishing communication.",
        "type": "string",
        "required": false,
        "valid_values": [
          "one_time_password",
          "without_password_not_secure",
          "cloud_token"
        ]
      },
      {
        "name": "priority",
        "description": "In a High Availability New mode cluster each machine is given a priority. The highest priority machine serves as the gateway in normal circumstances. If this machine fails, control is passed to the next highest priority machine. If that machine fails, control is passed to the next machine, and so on. In Load Sharing Unicast mode cluster, the highest priority is the pivot machine. The values must be in a range from 1 to N, where N is number of cluster members.",
        "type": "integer",
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
        "name": "os-name",
        "description": "Cluster platform operating system.",
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
        "name": "send-alerts-to-server",
        "description": "Server(s) to send alerts to.",
        "type": "Object",
        "required": false
      },
      {
        "name": "send-logs-to-backup-server",
        "description": "Backup server(s) to send logs to.",
        "type": "Object",
        "required": false
      },
      {
        "name": "send-logs-to-server",
        "description": "Server(s) to send logs to.",
        "type": "Object",
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
        "description": "Cluster platform version.",
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
        "name": "task-id",
        "description": "Task UID. Use show-task command to check the progress of the task.",
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
    "add-simple-cluster": {
      "description": "Add a simple cluster with two members and three interfaces",
      "request": "POST {{server}}/add-simple-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"cluster1\",\n  \"color\" : \"yellow\",\n  \"version\" : \"R80.30\",\n  \"ip-address\" : \"17.23.5.1\",\n  \"os-name\" : \"Gaia\",\n  \"cluster-mode\" : \"cluster-xl-ha\",\n  \"firewall\" : true,\n  \"vpn\" : false,\n  \"interfaces\" : [ {\n    \"name\" : \"eth0\",\n    \"ip-address\" : \"17.23.5.1\",\n    \"network-mask\" : \"255.255.255.0\",\n    \"interface-type\" : \"cluster\",\n    \"topology\" : \"EXTERNAL\",\n    \"anti-spoofing\" : true\n  }, {\n    \"name\" : \"eth1\",\n    \"interface-type\" : \"sync\",\n    \"topology\" : \"INTERNAL\",\n    \"topology-settings\" : {\n      \"ip-address-behind-this-interface\" : \"network defined by the interface ip and net mask\",\n      \"interface-leads-to-dmz\" : false\n    }\n  }, {\n    \"name\" : \"eth2\",\n    \"ip-address\" : \"192.168.1.1\",\n    \"network-mask\" : \"255.255.255.0\",\n    \"interface-type\" : \"cluster\",\n    \"topology\" : \"INTERNAL\",\n    \"anti-spoofing\" : true,\n    \"topology-settings\" : {\n      \"ip-address-behind-this-interface\" : \"network defined by the interface ip and net mask\",\n      \"interface-leads-to-dmz\" : false\n    }\n  } ],\n  \"members\" : [ {\n    \"name\" : \"member1\",\n    \"one-time-password\" : \"abcd\",\n    \"ip-address\" : \"17.23.5.2\",\n    \"interfaces\" : [ {\n      \"name\" : \"eth0\",\n      \"ip-address\" : \"17.23.5.2\",\n      \"network-mask\" : \"255.255.255.0\"\n    }, {\n      \"name\" : \"eth1\",\n      \"ip-address\" : \"1.1.2.4\",\n      \"network-mask\" : \"255.255.255.0\"\n    }, {\n      \"name\" : \"eth2\",\n      \"ip-address\" : \"192.168.1.2\",\n      \"network-mask\" : \"255.255.255.0\"\n    } ]\n  }, {\n    \"name\" : \"member2\",\n    \"one-time-password\" : \"abcd\",\n    \"ip-address\" : \"17.23.5.3\",\n    \"interfaces\" : [ {\n      \"name\" : \"eth0\",\n      \"ip-address\" : \"17.23.5.3\",\n      \"network-mask\" : \"255.255.255.0\"\n    }, {\n      \"name\" : \"eth1\",\n      \"ip-address\" : \"1.1.2.5\",\n      \"network-mask\" : \"255.255.255.0\"\n    }, {\n      \"name\" : \"eth2\",\n      \"ip-address\" : \"192.168.1.3\",\n      \"network-mask\" : \"255.255.255.0\"\n    } ]\n  } ]\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:09.106194",
    "source_file": "add-simple-cluster.html"
  }
}
```