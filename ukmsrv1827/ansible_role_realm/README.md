ansible-role-realm
=========

This role automates the process of joining a Red Hat Enterprise Linux (RHEL) system to an Active Directory domain and permit Active Directory Groups.

Requirements
------------

- RHEL system with access to necessary packages (realmd, sssd, oddjob, oddjob-mkhomedir, adcli, samba-common-tools, and python3-pexpect).
- User with sudo access to run the playbook and join the system to the domain.
- Valid Active Directory domain credentials.

Role Variables
--------------

Available variables are listed below, (see `vars/main.yml`):

```yaml
packages:
departments:
  department1:
    ou_name: OU=Computers,DC=example,DC=com
    ad_groups:
      - 'group1'
      - 'group2'
ad_user: ad_user
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: localhost
  gather_facts: true
  vars_prompt:
    - name: "ad_user"
      prompt: "Enter the Active Directory username"
      private: false

    - name: "ad_password"
      prompt: "Enter the Active Directory password"
      private: true
      no_log: true

    - name: "department"
      prompt: "Which department does the server belong to? (e.g., department1, department2)"
      private: false

  roles:
    - ansible-role-realm
```

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
