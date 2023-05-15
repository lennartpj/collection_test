Satellite Registration Role
=========

This Ansible role registers a RHEL server to a Red Hat Satellite server using a registration link.

Requirements
------------
none.
Role Variables
--------------

The role uses the following variables:

`activation_key_input`: An integer representing the index (1-based) of the desired registration link in the `satellite_links` list defined in the role's `vars/main.yml`.
If `activation_key_input` is not provided when calling the role, the role will prompt for it during execution.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------
Here's an example playbook that uses this role:

```yaml
---
---
- hosts: localhost
  vars_prompt:
    - name: "activation_key_input"
      prompt: "Please select an option for the registration key: 1) Key 1 2) Key 2 3) Key 3"
      private: no
  roles:
    - satellite_register
```

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
