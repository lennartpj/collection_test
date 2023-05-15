ansible_role_network_settings
=========

This role is used to set the network settings of a Red Hat Enterprise Linux (RHEL) system. It prompts the user for the IPv4 address and gateway, then uses these inputs to configure the network settings of the system.

Requirements
------------

none

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

ipv4_dns (default: <default_ipv4_dns1>, <default_ipv4_dns2>): List of DNS servers to use for IPv4.
ipv4_dns_search (default: example.com): DNS search domain for IPv4.
ipv6_method (default: auto): Method for IPv6 address assignment.
ipv4_method (default: manual): Method for IPv4 address assignment.
connection_interface_name (default: ens192): Network interface name.
connection_zone (default: public): Firewall zone for the connection.

Dependencies
------------

rhel-system-roles.network

Example Playbook
----------------

```yml
- hosts: servers
  roles:
     - ansible_role_network_settings
```
License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
