# set-lsm-cluster

```json
{
  "command": "set-lsm-cluster",
  "description": "Edit existing LSM Cluster.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-lsm-cluster",
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
        "name": "dynamic-objects",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "resolved-ip-addresses",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "resolved-ip-addresses",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "resolved-ip-addresses",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "resolved-ip-addresses",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": true
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "name",
        "description": "Interface name.",
        "type": "string",
        "required": true
      },
      {
        "name": "new-name",
        "description": "New name. Overrides the interface name on profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address-override",
        "description": "IP address override. Net mask is defined by the attached LSM profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "member-network-override",
        "description": "Member network override. Net mask is defined by the attached LSM profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "members",
        "description": "",
        "type": "array",
        "required": false,
        "default": "black",
        "valid_values": [
          "off",
          "manual",
          "using-profile"
        ]
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "device-id",
        "description": "Device ID.",
        "type": "string",
        "required": false
      },
      {
        "name": "provisioning-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "provisioning-profile",
        "description": "Provisioning profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "provisioning-state",
        "description": "Provisioning state. This field is relevant just for SMB clusters. By default the state is 'manual'- enable provisioning but not attach to profile.If 'using-profile' state is provided a provisioning profile must be provided in provisioning-settings.",
        "type": "string",
        "required": false,
        "valid_values": [
          "off",
          "manual",
          "using-profile"
        ]
      },
      {
        "name": "sic",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "one-time-password",
        "description": "One-time password. When one-time password is provided without ip-address- trusted communication is automatically initiated when the gateway connects to the Security Management server for the first time.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IP address. When IP address is provided- initiate trusted communication immediately using this IP address.",
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
        "name": "domains-to-process",
        "description": "Indicates which domains to process the commands on. It cannot be used with the details-level full, must be run from the System Domain only and with ignore-warnings true. Valid values are: CURRENT_DOMAIN, ALL_DOMAINS_ON_THIS_SERVER.",
        "type": "array",
        "required": false,
        "default": "CURRENT_DOMAIN"
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "string",
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
        "name": "topology",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "not-defined",
          "external-ip-addresses-only",
          "hide-behind-gateway-external-ip-address",
          "all-ip-addresses-behind-the-gateway",
          "manual"
        ]
      },
      {
        "name": "manual-vpn-domain",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
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
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-domain",
        "description": "VPN Domain type. 'external-interfaces-only' is relevnt only for Gaia devices. 'hide-behind-gateway-external-ip-address' is relevant only for SMB devices.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not-defined",
          "external-ip-addresses-only",
          "hide-behind-gateway-external-ip-address",
          "all-ip-addresses-behind-the-gateway",
          "manual"
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
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "dynamic-objects",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "comments",
        "description": "Comments.",
        "type": "string",
        "required": false
      },
      {
        "name": "name",
        "description": "Name.",
        "type": "string",
        "required": false
      },
      {
        "name": "resolved-ip-addresses",
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
        "name": "ipv4-address-range",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "From IPv4 Address.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "To IPv4 Address.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "name",
        "description": "Interface Name.",
        "type": "string",
        "required": false
      },
      {
        "name": "cluster-ip-address-override",
        "description": "Cluster IP address override.",
        "type": "string",
        "required": false
      },
      {
        "name": "member-network-override",
        "description": "Member network override.",
        "type": "string",
        "required": false
      },
      {
        "name": "main-ip-address",
        "description": "Main ip-address.",
        "type": "string",
        "required": false
      },
      {
        "name": "members",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "off",
          "manual",
          "using-profile"
        ]
      },
      {
        "name": "member-name",
        "description": "Member name. Consists of the member name in the LSM profile and the prefix or suffix of the cluster.",
        "type": "string",
        "required": false
      },
      {
        "name": "member-uid",
        "description": "Member uid.",
        "type": "string",
        "required": false
      },
      {
        "name": "device-id",
        "description": "Device ID.",
        "type": "string",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "IP address.",
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
        "name": "main-ip-address",
        "description": "Main ip address.",
        "type": "string",
        "required": false
      },
      {
        "name": "provisioning-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "provisioning-profile",
        "description": "Attached provisioning profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "provisioning-state",
        "description": "Provisioning state.",
        "type": "string",
        "required": false,
        "valid_values": [
          "off",
          "manual",
          "using-profile"
        ]
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
        "required": false
      },
      {
        "name": "gateway-status",
        "description": "The current status of the Cluster member. Shown only when the 'show-statuses' parameter is set to 'true'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ok",
          "waiting",
          "unknown",
          "untrusted",
          "not-responding",
          "needs-attention"
        ]
      },
      {
        "name": "last-applied-provisioning-settings-time",
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
        "name": "last-policy-fetch-time",
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
        "name": "last-provisioning-settings-sync-time",
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
        "name": "policy-status",
        "description": "The current status of the Security Policy. Shown only when the 'show-statuses' parameter is set to 'true'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ok",
          "waiting",
          "unknown",
          "untrusted",
          "not-responding",
          "needs-attention",
          "not-installed",
          "not-updated",
          "may-be-out-of-date"
        ]
      },
      {
        "name": "provisioning-settings-status",
        "description": "The current status of the Provisioning Settings. Shown only when the 'show-statuses' parameter is set to 'true'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ok",
          "unknown",
          "needs-attention",
          "maintenance-mode",
          "error",
          "downloading-firmware",
          "downloaded-firmware",
          "installing-firmware",
          "installation-finished-rebooting",
          "revert",
          "installation-failed-reverting",
          "reverted-rebooting",
          ""
        ]
      },
      {
        "name": "os-name",
        "description": "Device platform operating system.",
        "type": "string",
        "required": false
      },
      {
        "name": "security-profile",
        "description": "Attached LSM profile.",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "manual-vpn-domain",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "comments",
        "description": "comments.",
        "type": "string",
        "required": false
      },
      {
        "name": "from-ipv4-address",
        "description": "First IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "to-ipv4-address",
        "description": "Last IPv4 address of the IP address range.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-domain",
        "description": "VPN domain type.",
        "type": "string",
        "required": false
      },
      {
        "name": "version",
        "description": "Device platform version.",
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
    "set lsm cluster add dynamic objects and topology": {
      "description": "",
      "request": "POST {{server}}/add-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"lsm_cluster\",\n  \"dynamic-objects\" : {\n    \"add\" : {\n      \"name\" : \"dynamic-object-name\",\n      \"resolved-ip-addresses\" : {\n        \"add\" : {\n          \"ipv4-address\" : \"10.10.10.1\"\n        }\n      }\n    }\n  },\n  \"topology\" : {\n    \"vpn-domain\" : \"manual\",\n    \"manual-vpn-domain\" : {\n      \"add\" : {\n        \"from-ipv4-address\" : \"10.10.10.1\",\n        \"to-ipv4-address\" : \"10.10.10.2\",\n        \"comments\" : \"range 1\"\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set lsm cluster remove dynamic object": {
      "description": "",
      "request": "POST {{server}}/add-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"lsm_cluster\",\n  \"dynamic-objects\" : {\n    \"remove\" : {\n      \"name\" : \"dynamic_object_name\"\n    }\n  }\n}",
      "response": ""
    },
    "set lsm cluster remove dynamic object range": {
      "description": "",
      "request": "POST {{server}}/add-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"lsm_cluster\",\n  \"dynamic-objects\" : {\n    \"set\" : {\n      \"name\" : \"dynamic_object_name\",\n      \"resolved-ip-addresses\" : {\n        \"remove\" : {\n          \"ipv4-address\" : \"10.10.10.1\"\n        }\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set lsm cluster remove topology vpn domain": {
      "description": "",
      "request": "POST {{server}}/add-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"lsm_cluster\",\n  \"topology\" : {\n    \"manual-vpn-domain\" : {\n      \"remove\" : {\n        \"from-ipv4-address\" : \"10.10.10.1\",\n        \"to-ipv4-address\" : \"10.10.10.2\",\n        \"comments\" : \"range 1\"\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set-lsm-gaia-cluster": {
      "description": "",
      "request": "POST {{server}}/set-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Gaia_gaia_cluster\",\n  \"interfaces\" : [ {\n    \"name\" : \"eth0\",\n    \"new-name\" : \"WAN\",\n    \"member-network-override\" : \"192.168.8.0\",\n    \"ip-address-override\" : \"192.168.8.197\"\n  }, {\n    \"name\" : \"eth1\",\n    \"new-name\" : \"LAN1\",\n    \"member-network-override\" : \"10.8.197.0\",\n    \"ip-address-override\" : \"10.8.197.1\"\n  }, {\n    \"name\" : \"eth2\",\n    \"member-network-override\" : \"10.10.10.0\"\n  } ],\n  \"members\" : [ {\n    \"name\" : \"Gaia_gw1\",\n    \"sic\" : {\n      \"ip-address\" : \"192.168.8.200\",\n      \"one-time-password\" : \"aaaa\"\n    }\n  }, {\n    \"name\" : \"Gaia_gw2\",\n    \"sic\" : {\n      \"ip-address\" : \"192.168.8.202\",\n      \"one-time-password\" : \"aaaa\"\n    }\n  } ]\n}",
      "response": ""
    },
    "set-lsm-smb-cluster": {
      "description": "",
      "request": "POST {{server}}/set-lsm-cluster\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"smb_smb_cluster\",\n  \"interfaces\" : [ {\n    \"name\" : \"eth0\",\n    \"new-name\" : \"WAN\",\n    \"member-network-override\" : \"192.168.8.0\",\n    \"ip-address-override\" : \"192.168.8.197\"\n  }, {\n    \"name\" : \"eth1\",\n    \"new-name\" : \"LAN1\",\n    \"member-network-override\" : \"10.8.197.0\",\n    \"ip-address-override\" : \"10.8.197.1\"\n  }, {\n    \"name\" : \"eth2\",\n    \"member-network-override\" : \"10.10.10.0\"\n  } ],\n  \"members\" : [ {\n    \"name\" : \"smb_gw1\",\n    \"sic\" : {\n      \"ip-address\" : \"192.168.8.200\",\n      \"one-time-password\" : \"aaaa\"\n    },\n    \"provisioning-state\" : \"using-profile\",\n    \"provisioning-settings\" : {\n      \"provisioning-profile\" : \"prv_profile\"\n    }\n  }, {\n    \"name\" : \"smb_gw2\",\n    \"sic\" : {\n      \"ip-address\" : \"192.168.8.202\",\n      \"one-time-password\" : \"aaaa\"\n    },\n    \"provisioning-state\" : \"using-profile\",\n    \"provisioning-settings\" : {\n      \"provisioning-profile\" : \"smb_prv_profile\"\n    }\n  } ]\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.950939",
    "source_file": "set-lsm-cluster.html"
  }
}
```