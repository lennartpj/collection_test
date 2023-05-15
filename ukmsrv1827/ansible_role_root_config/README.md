ansible_role_root_config
=========

This Ansible role changes the root password of a RHEL server and sets PermitRootLogin to 'no' in the sshd_config file. If the new root password isn't defined in a vars_prompt in the executing playbook, the role prompts for the new root password.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    new_root_password: ""

The new root password. If this is not set, the role will prompt for it.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
    
    - hosts: servers
      roles:
         - root_config
      vars_prompt:
        - name: "new_root_password"
          prompt: "What should the new root password be?"
          private: yes

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
