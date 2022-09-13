Ansible Role: install_httpd_service
=========

Install httpd packages, deploy httpd.conf and open http port on firewalld.

Installation
------------

```shell
$ ansible-galaxy install install_httpd_service
```

To be able to update later and eventually to modify it, prefer using `requirements.yml` with the git source:

```yaml
- name: install_httpd_service
  src: git@github.com:sup-computersysteme-gmbh/ansible-role-install-httpd-service.git
  scm: git
  version: main
```
And then download it with `ansible-galaxy`:

```shell
$ ansible-galaxy install -r requirements.yml
```

Using `git`, you'll have to be carefull to folder name:

```shell
$ git clone git@github.com:sup-computersysteme-gmbh/ansible-role-install-httpd-service.git install_httpd_service
```

Role Variables
--------------

Available variables are listed below, along with their default values (see `defaults/main.yml`):

Default:
 ```yaml
rhel_httpd_packages:
  - httpd.x86_64
  - httpd-tools.x86_64
 ```

Ansible Facts:
- ansible_distribution
- ansible_distribution_major_version

Dependencies
------------

see `meta/requirements.yml`
