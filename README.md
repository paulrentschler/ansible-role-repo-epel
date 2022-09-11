paulrentschler.repo-epel
========================

[![MIT licensed][mit-badge]][mit-link]

Installs the [EPEL repository](https://fedoraproject.org/wiki/EPEL) (Extra Packages for Enterprise Linux) on RedHat/CentOS Linux machines.


Requirements
------------

None.


Role Variables
--------------

The following variables are available with defaults defined in `defaults/main.yml`:

The repo URL and GPG key urls. These should not need to be readily changed but they can be overridden to use a specific version or a completely different repo.

    epel_repo_url: "https://dl.fedoraproject.org/pub/epel/epel-release-latest-{{ ansible_distribution_major_version }}.noarch.rpm"
    epel_repo_gpg_key_url: "https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-{{ ansible_distribution_major_version }}"


The file that contains the repo configuration information that adds it to YUM

    epel_repofile_path: "/etc/yum.repos.d/epel.repo"


Set to `true` to disable the EPEL repo even if it is already installed.

    epel_repo_disable: false


Dependencies
------------

None.


Example Playbook
----------------

Simple version:

```yaml
---
- hosts: all
  roles:
    - paulrentschler.repo-epel
```


License
-------

[MIT][mit-link]


Author Information
------------------

Created by Paul Rentschler in 2022.

Based heavily on the [geerlingguy.repo-epel](https://galaxy.ansible.com/geerlingguy/repo-epel) role created by [Jeff Geerling](https://www.jeffgeerling.com/).


[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://github.com/paulrentschler/ansible-role-redis/blob/main/LICENSE
