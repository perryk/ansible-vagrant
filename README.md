vagrant
=========

[![pipeline status](https://gitlab.com/devoperate/ansible-vagrant/badges/master/pipeline.svg)](https://gitlab.com/devoperate/ansible-vagrant/commits/master)

Installs any version of Vagrant securely by verifying cryptographic signatures on distribution archives with GPG and SHA256 hash comparison.

Requirements
------------

The target host must run Linux.

Role Variables
--------------

Any version of Vagrant can be installed by changing the `vagrant_version` variable's value to just the SemVer of the version you want to install. Overriding this variable and re-running the role can up/downgrade Vagrant on the target host.

Dependencies
------------

See meta/main.yml.

Example Playbook
----------------

```yaml
- hosts: localhost
  roles:
    - role: devoperate.vagrant
      vars:
        vagrant_version: '0.11.11'
```

License
-------

See LICENSE.

Author Information
------------------

- [Claude Léveillé](https://claude-leveille.com)
