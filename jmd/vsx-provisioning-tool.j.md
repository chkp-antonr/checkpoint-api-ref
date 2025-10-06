# vsx-provisioning-tool

```json
{
  "command": "vsx-provisioning-tool",
  "description": "Run the VSX provisioning tool with the specified parameters. Important note: An automatic session publish is part of all the operations in this API.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/vsx-provisioning-tool",
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
        "name": "operation",
        "description": "The name of the provisioning operation to run. Each operation has its own specific parameters. The available operations are:add-vsx-gateway - Adds a new VSX gatewayadd-vsx-cluster - Adds a new VSX cluster*add-vsx-cluster-member - Adds a new VSX cluster member*add-vd - Adds a new Virtual Device (VS/VSB/VSW/VR) to a VSX gateway or VSX clusteradd-vd-interface - Adds a new virtual interface to a Virtual Deviceadd-physical-interface - Adds a physical interface to a VSX gateway or VSX clusteradd-route - Adds a route to a Virtual Deviceattach-bridge - Attaches a bridge interface to a Virtual Systemremove-vsx - Removes a VSX gateway or VSX clusterremove-vd - Removes a Virtual Deviceremove-vd-interface - Removes an interface from a Virtual Deviceremove-physical-interface - Removes a physical interface from a VSX gateway or VSX clusterremove-route - Removes a route from a Virtual Deviceset-vd - Modifies a Virtual Deviceset-vd-interface - Modifies an interface on a Virtual Deviceset-physical-interface - Modifies a physical interface on a VSX cluster or VSX gateway * When adding a VSX Cluster, you must also add at least 2 cluster members * Adding cluster members is only allowed when adding a new VSX cluster * To add members to an existing cluster, use vsx-run-operation.",
        "type": "string",
        "required": true,
        "valid_values": [
          "attach-bridge",
          "add-route",
          "add-physical-interface",
          "add-vd-interface",
          "add-vsx-gateway",
          "add-vsx-cluster",
          "add-vd",
          "remove-route",
          "remove-vd",
          "remove-vsx",
          "remove-physical-interface",
          "remove-vd-interface",
          "set-vd",
          "set-physical-interface",
          "set-vd-interface"
        ]
      },
      {
        "name": "add-physical-interface-params",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "name",
        "description": "Name of the interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "vlan-trunk",
        "description": "True if this interface is a VLAN trunk.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "add-route-params",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "destination",
        "description": "Route destination. To specify the default route, use 'default' for IPv4 and 'default6' for IPv6.",
        "type": "string",
        "required": true
      },
      {
        "name": "next-hop",
        "description": "Next hop IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "netmask",
        "description": "Subnet mask for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "prefix",
        "description": "CIDR prefix for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate this route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "add-vd-interface-params",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "leads-to",
        "description": "Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "The anti-spoofing enforcement setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "anti-spoofing-tracking",
        "description": "The anti-spoofing tracking setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "alert",
          "log"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address of this interface with optional CIDR prefix.Required if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-netmask",
        "description": "IPv4 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-prefix",
        "description": "IPv4 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 Address of this interfaceRequired if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-netmask",
        "description": "IPv6 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-prefix",
        "description": "IPv6 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "mtu",
        "description": "MTU of this interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate IPv4 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "propagate6",
        "description": "Propagate IPv6 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "specific-group",
        "description": "Specific group for interface topology.Only for use with topology option 'internal_specific'.",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "Topology of this interface.Automatic topology calculation based on routes must be disabled for this VS.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal_undefined",
          "internal_this_network",
          "internal_specific",
          "defined_by_routes"
        ]
      },
      {
        "name": "vti-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "local-ipv4-address",
        "description": "The IPv4 address of the VPN tunnel on this Virtual System.",
        "type": "string",
        "required": true
      },
      {
        "name": "peer-name",
        "description": "The name of the remote peer object as defined in the VPN community.",
        "type": "string",
        "required": true
      },
      {
        "name": "remote-ipv4-address",
        "description": "The IPv4 address of the VPN tunnel on the remote VPN peer.",
        "type": "string",
        "required": true
      },
      {
        "name": "tunnel-id",
        "description": "Optional unique Tunnel ID.Automatically assigned by the system if empty.",
        "type": "string",
        "required": false
      },
      {
        "name": "add-vd-params",
        "description": "",
        "type": "array",
        "required": false,
        "default": "false",
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "Object",
        "required": true,
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "leads-to",
        "description": "Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "The anti-spoofing enforcement setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "anti-spoofing-tracking",
        "description": "The anti-spoofing tracking setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "alert",
          "log"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address of this interface with optional CIDR prefix.Required if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-netmask",
        "description": "IPv4 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-prefix",
        "description": "IPv4 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 Address of this interfaceRequired if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-netmask",
        "description": "IPv6 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-prefix",
        "description": "IPv6 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "mtu",
        "description": "MTU of this interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate IPv4 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "propagate6",
        "description": "Propagate IPv6 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "specific-group",
        "description": "Specific group for interface topology.Only for use with topology option 'internal_specific'.",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "Topology of this interface.Automatic topology calculation based on routes must be disabled for this VS.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal_undefined",
          "internal_this_network",
          "internal_specific",
          "defined_by_routes"
        ]
      },
      {
        "name": "leads-to",
        "description": "Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "The anti-spoofing enforcement setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "anti-spoofing-tracking",
        "description": "The anti-spoofing tracking setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "alert",
          "log"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address of this interface with optional CIDR prefix.Required if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-netmask",
        "description": "IPv4 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-prefix",
        "description": "IPv4 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 Address of this interfaceRequired if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-netmask",
        "description": "IPv6 Subnet mask of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-prefix",
        "description": "IPv6 CIDR prefix of this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "mtu",
        "description": "MTU of this interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate IPv4 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "propagate6",
        "description": "Propagate IPv6 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "specific-group",
        "description": "Specific group for interface topology.Only for use with topology option 'internal_specific'.",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "Topology of this interface.Automatic topology calculation based on routes must be disabled for this VS.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal_undefined",
          "internal_this_network",
          "internal_specific",
          "defined_by_routes"
        ]
      },
      {
        "name": "type",
        "description": "Type of the Virtual Device vs - Virtual Firewallvr - Virtual Routervsw - Virtual Switchvsbm - Virtual Firewall in bridge mode.",
        "type": "string",
        "required": true,
        "valid_values": [
          "vs",
          "vr",
          "vsw",
          "vsbm"
        ]
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "calc-topology-auto",
        "description": "Calculate interface topology automatically based on routes.Relevant only for Virtual Systems.Do not use for virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address.Required if this device is a Virtual System.Do not use for other virtual devices.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-instances",
        "description": "Number of IPv4 instances for the Virtual System.Must be greater or equal to 1.Only relevant for Virtual Systems and Virtual Systems in bridge mode.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address.Required if this device is a Virtual System.Do not use for other virtual devices.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-instances",
        "description": "Number of IPv6 instances for the Virtual System.Only relevant for Virtual Systems and Virtual Systems in bridge mode.",
        "type": "integer",
        "required": false
      },
      {
        "name": "routes",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "destination",
        "description": "Route destination. To specify the default route, use 'default' for IPv4 and 'default6' for IPv6.",
        "type": "string",
        "required": true
      },
      {
        "name": "next-hop",
        "description": "Next hop IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "netmask",
        "description": "Subnet mask for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "prefix",
        "description": "CIDR prefix for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate this route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "destination",
        "description": "Route destination. To specify the default route, use 'default' for IPv4 and 'default6' for IPv6.",
        "type": "string",
        "required": true
      },
      {
        "name": "next-hop",
        "description": "Next hop IP address.",
        "type": "string",
        "required": true
      },
      {
        "name": "netmask",
        "description": "Subnet mask for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "prefix",
        "description": "CIDR prefix for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate this route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "vs-mtu",
        "description": "MTU of the Virtual System.Only relevant for Virtual Systems in bridge mode.Do not use for other virtual devices.",
        "type": "integer",
        "required": false
      },
      {
        "name": "add-vsx-cluster-params",
        "description": "",
        "type": "array",
        "required": false,
        "default": "enable",
        "valid_values": [
          "vsls",
          "ha"
        ]
      },
      {
        "name": "cluster-type",
        "description": "Cluster type for the VSX Cluster Object.Starting in R81.10, only VSLS can be configured during cluster creation.To use High Availability ('ha'), first create the cluster as VSLS and then run vsx_util on the Management.",
        "type": "string",
        "required": true,
        "valid_values": [
          "vsls",
          "ha"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address of the VSX Gateway or Cluster object.Optional if main IPv6 Address is defined.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address of the VSX Gateway or Cluster object.Optional if main IPv4 Address is defined.",
        "type": "string",
        "required": true
      },
      {
        "name": "members",
        "description": "",
        "type": "Object",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address of the VSX Cluster member.Mandatory if the VSX Cluster has an IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address of the VSX Cluster member.Mandatory if the VSX Cluster has an IPv6 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "name",
        "description": "Name of the new VSX Cluster member.",
        "type": "string",
        "required": true
      },
      {
        "name": "sic-otp",
        "description": "SIC one-time-password of the VSX Gateway or Cluster member.Password must be between 4-127 characters in length.",
        "type": "string",
        "required": true
      },
      {
        "name": "sync-ip",
        "description": "Sync IP address for the VSX Cluster member.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address of the VSX Cluster member.Mandatory if the VSX Cluster has an IPv4 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address of the VSX Cluster member.Mandatory if the VSX Cluster has an IPv6 Address.",
        "type": "string",
        "required": true
      },
      {
        "name": "name",
        "description": "Name of the new VSX Cluster member.",
        "type": "string",
        "required": true
      },
      {
        "name": "sic-otp",
        "description": "SIC one-time-password of the VSX Gateway or Cluster member.Password must be between 4-127 characters in length.",
        "type": "string",
        "required": true
      },
      {
        "name": "sync-ip",
        "description": "Sync IP address for the VSX Cluster member.",
        "type": "string",
        "required": true
      },
      {
        "name": "sync-if-name",
        "description": "Sync interface name for the VSX Cluster.",
        "type": "string",
        "required": true
      },
      {
        "name": "sync-netmask",
        "description": "Sync interface netmask for the VSX Cluster.",
        "type": "string",
        "required": true
      },
      {
        "name": "version",
        "description": "Version of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "rule-drop",
        "description": "Add a default drop rule to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "enable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-https",
        "description": "Add a rule to allow HTTPS traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ping",
        "description": "Add a rule to allow ping traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ping6",
        "description": "Add a rule to allow ping6 traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-snmp",
        "description": "Add a rule to allow SNMP traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ssh",
        "description": "Add a rule to allow SSH traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "add-vsx-gateway-params",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "enable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address of the VSX Gateway or Cluster object.Optional if main IPv6 Address is defined.",
        "type": "string",
        "required": true
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address of the VSX Gateway or Cluster object.Optional if main IPv4 Address is defined.",
        "type": "string",
        "required": true
      },
      {
        "name": "sic-otp",
        "description": "SIC one-time-password of the VSX Gateway or Cluster member.Password must be between 4-127 characters in length.",
        "type": "string",
        "required": true
      },
      {
        "name": "version",
        "description": "Version of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "rule-drop",
        "description": "Add a default drop rule to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "enable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-https",
        "description": "Add a rule to allow HTTPS traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ping",
        "description": "Add a rule to allow ping traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ping6",
        "description": "Add a rule to allow ping6 traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-snmp",
        "description": "Add a rule to allow SNMP traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "rule-ssh",
        "description": "Add a rule to allow SSH traffic to the VSX Gateway or Cluster initial policy.",
        "type": "string",
        "required": false,
        "default": "disable",
        "valid_values": [
          "enable",
          "disable"
        ]
      },
      {
        "name": "attach-bridge-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ifs1",
        "description": "Name of the first interface for the bridge.",
        "type": "string",
        "required": true
      },
      {
        "name": "ifs2",
        "description": "Name of the second interface for the bridge.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove-physical-interface-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "name",
        "description": "Name of the interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove-route-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "destination",
        "description": "Route destination. To specify the default route, use 'default' for IPv4 and 'default6' for IPv6.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "netmask",
        "description": "Subnet mask for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "prefix",
        "description": "CIDR prefix for this route.",
        "type": "string",
        "required": false
      },
      {
        "name": "remove-vd-interface-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "leads-to",
        "description": "Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove-vd-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove-vsx-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "set-physical-interface-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "name",
        "description": "Name of the interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vlan-trunk",
        "description": "True if this interface is a VLAN trunk.",
        "type": "boolean",
        "required": true
      },
      {
        "name": "vsx-name",
        "description": "Name of the VSX Gateway or Cluster object.",
        "type": "string",
        "required": true
      },
      {
        "name": "set-vd-interface-params",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "leads-to",
        "description": "Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": true
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "The anti-spoofing enforcement setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect",
          "off"
        ]
      },
      {
        "name": "anti-spoofing-tracking",
        "description": "The anti-spoofing tracking setting of this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "alert",
          "log"
        ]
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 Address of this interface with optional CIDR prefix.Required if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 Address of this interfaceRequired if this interface belongs to a Virtual System or Virtual Router.",
        "type": "string",
        "required": false
      },
      {
        "name": "mtu",
        "description": "MTU of this interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "new-leads-to",
        "description": "New Virtual Switch or Virtual Router for this interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "propagate",
        "description": "Propagate IPv4 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "propagate6",
        "description": "Propagate IPv6 route to adjacent virtual devices.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "specific-group",
        "description": "Specific group for interface topology.Only for use with topology option 'internal_specific'.",
        "type": "string",
        "required": false
      },
      {
        "name": "topology",
        "description": "Topology of this interface.Automatic topology calculation based on routes must be disabled for this VS.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal_undefined",
          "internal_this_network",
          "internal_specific",
          "defined_by_routes"
        ]
      },
      {
        "name": "set-vd-params",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "vd",
        "description": "Name of the Virtual System, Virtual Switch, or Virtual Router.",
        "type": "string",
        "required": true
      },
      {
        "name": "calc-topology-auto",
        "description": "Calculate interface topology automatically based on routes.Relevant only for Virtual Systems.Do not use for virtual devices.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "Main IPv4 Address.Relevant only if this device is a Virtual System.Do not use for other virtual devices.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-instances",
        "description": "Number of IPv4 instances for the Virtual System.Must be greater or equal to 1.Only relevant for Virtual Systems and Virtual Systems in bridge mode.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "Main IPv6 Address.Relevant only if this device is a Virtual System.Do not use for other virtual devices.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-instances",
        "description": "Number of IPv6 instances for the Virtual System.Only relevant for Virtual Systems and Virtual Systems in bridge mode.",
        "type": "integer",
        "required": false
      },
      {
        "name": "vs-mtu",
        "description": "MTU of the Virtual System.Only relevant for Virtual Systems in bridge mode.Do not use for other virtual devices.",
        "type": "integer",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Operation task UID. Use the show-task command to check the progress of the task.",
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
    "vsx-provisioning-tool add-vsx-cluster": {
      "description": "Add a VSX cluster with 2 cluster members",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-vsx-cluster\",\n  \"add-vsx-cluster-params\" : {\n    \"vsx-name\" : \"VSX_CLUSTER\",\n    \"cluster-type\" : \"vsls\",\n    \"version\" : \"R81.10\",\n    \"ipv4-address\" : \"10.1.1.15\",\n    \"sync-if-name\" : \"eth3\",\n    \"sync-netmask\" : \"255.255.255.0\",\n    \"rule-ping\" : \"enable\",\n    \"rule-drop\" : \"enable\",\n    \"members\" : [ {\n      \"name\" : \"VSX1\",\n      \"ipv4-address\" : \"10.1.1.1\",\n      \"sync-ip\" : \"192.168.1.1\",\n      \"sic-otp\" : \"sicotp123\"\n    }, {\n      \"name\" : \"VSX2\",\n      \"ipv4-address\" : \"10.1.1.2\",\n      \"sync-ip\" : \"192.168.1.2\",\n      \"sic-otp\" : \"sicotp123\"\n    } ]\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool add IPv4 default route": {
      "description": "Add a new IPv4 default route",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-route\",\n  \"add-route-params\" : {\n    \"destination\" : \"default\",\n    \"next-hop\" : \"192.168.1.254\",\n    \"vd\" : \"VS1\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool add IPv4 route leading to VR": {
      "description": "Add a new IPv4 route leading to a Virtual Router",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-route\",\n  \"add-route-params\" : {\n    \"destination\" : \"10.1.1.0/24\",\n    \"leads-to\" : \"VR\",\n    \"vd\" : \"VS1\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool add-physical-interface": {
      "description": "Add a new physical interface to a VSX Gateway",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-physical-interface\",\n  \"add-physical-interface-params\" : {\n    \"name\" : \"eth3\",\n    \"vlan-trunk\" : \"false\",\n    \"vsx-name\" : \"VSX-GW\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool add-vd": {
      "description": "Add a new Virtual System to an existing VSX cluster",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-vd\",\n  \"add-vd-params\" : {\n    \"vd\" : \"NEW_VD\",\n    \"vsx-name\" : \"VSX_CLUSTER\",\n    \"type\" : \"vs\",\n    \"ipv4-instances\" : \"2\",\n    \"ipv4-address\" : \"192.168.1.1\",\n    \"interfaces\" : {\n      \"1\" : {\n        \"name\" : \"eth1\",\n        \"ipv4-address\" : \"192.168.1.1/24\"\n      }\n    }\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool add-vd-interface": {
      "description": "Add a new interface to a Virtual System",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"add-vd-interface\",\n  \"add-vd-interface-params\" : {\n    \"name\" : \"eth3\",\n    \"ipv4-address\" : \"192.168.1.1/24\",\n    \"vd\" : \"VS1\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool attach-bridge": {
      "description": "Attach a bridge interface to an existing Virtual System",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"attach-bridge\",\n  \"attach-bridge-params\" : {\n    \"vd\" : \"VS1\",\n    \"ifs1\" : \"eth6\",\n    \"ifs2\" : \"eth7\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool remove-physical-interface": {
      "description": "Remove a physical interface from a VSX Gateway",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"remove-physical-interface\",\n  \"remove-physical-interface-params\" : {\n    \"vsx-name\" : \"VSX_GATEWAY\",\n    \"name\" : \"eth2\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool remove-route": {
      "description": "Remove a route",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"remove-route\",\n  \"remove-route-params\" : {\n    \"vd\" : \"VS1\",\n    \"destination\" : \"192.168.1.0/24\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool remove-vd": {
      "description": "Remove an existing Virtual Device",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"remove-vd\",\n  \"remove-vd-params\" : {\n    \"vd\" : \"VS1\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool remove-vd-interface": {
      "description": "Remove an interface from a Virtual System",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"remove-vd-interface\",\n  \"remove-vd-interface\" : {\n    \"vd\" : \"VS1\",\n    \"name\" : \"eth3\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool remove-vsx": {
      "description": "Remove a VSX Gateway",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"remove-vsx\",\n  \"remove-vsx-params\" : {\n    \"vsx-name\" : \"VSX_GATEWAY\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool set-physical-interface": {
      "description": "Change the configuration of a physical interface",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"set-physical-interface\",\n  \"set-physical-interface-params\" : {\n    \"name\" : \"eth3\",\n    \"vlan-trunk\" : \"true\",\n    \"vsx-name\" : \"VSX-GW\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool set-vd": {
      "description": "Change the configuration of an existing Virtual System",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"set-vd\",\n  \"set-vd-params\" : {\n    \"ipv4-instances\" : \"3\",\n    \"ipv6-instances\" : \"2\",\n    \"vd\" : \"VS1\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    },
    "vsx-provisioning-tool set-vd-interface": {
      "description": "Change the configuration of an interface on a Virtual Device",
      "request": "POST {{server}}/vsx-provisioning-tool\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"operation\" : \"set-vd-interface\",\n  \"set-vd-interface-params\" : {\n    \"name\" : \"eth3\",\n    \"anti-spoofing\" : \"detect\",\n    \"vd\" : \"VS1\",\n    \"anti-spoofing-tracking\" : \"alert\",\n    \"mtu\" : \"1350\"\n  }\n}",
      "response": "{\n  \"task-id\" : \"01234567-89ab-abcd-1234-58dc02112100\"\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:30.005107",
    "source_file": "vsx-provisioning-tool.html"
  }
}
```