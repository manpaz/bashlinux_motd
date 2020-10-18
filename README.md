Bashlinux Baseline
==================

Minimal setup for each provisioned host including operational accounts and monitoring configuration.

Requirements
------------

Everything is covered by Ansible itself.


Role Variables
--------------

- meta.company:			Company or customer name
- meta.license:			License type which this role is distributed with
- meta.min_ansible_version:	Minimin Ansible's version this role is intended for.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

LGPL-3.0

Author Information
------------------

Manuel F Martinez <manpaz@bashlinux.com>
