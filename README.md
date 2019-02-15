vagrant
=========

[![pipeline status](https://gitlab.com/devoperate/ansible-vagrant/badges/master/pipeline.svg)](https://gitlab.com/devoperate/ansible-vagrant/commits/master)

Installs any version of Vagrant securely by verifying cryptographic signatures on distribution archives with GPG and SHA256 hash comparison.

Requirements
------------

The target host must run Linux.

Role Variables
--------------

<table>
  <tr>
    <th>Variable</th>
    <th>Data Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>vagrant_version</td>
    <td>string</td>
    <td>The desired version of Vagrant. Note that downgrades are not possible unless you manually or otherwise purge the current Vagrant installation beforehand.</td>
  </tr>
</table>

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
        vagrant_version: '2.2.3'
```

License
-------

See LICENSE.

Author Information
------------------

- [Claude Léveillé](https://claude-leveille.com)
