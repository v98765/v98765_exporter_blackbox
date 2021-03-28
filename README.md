Ansible role : blackbox_exporter
=========

Deploy and configure prometheus blackbox_exporter

Requirements
------------

Ansible, ubuntu

Role Variables
--------------

Name | Default Value | Description
---|---|---
`blackbox_exporter_version` |  "0.18.0" | current version
`blackbox_exporter_system_user` | "blackbox-exp" |
`blackbox_exporter_system_group` | "blackbox-exp" |
`blackbox_exporter_install_dir` |  "/usr/local/bin" |
`blackbox_exporter_repo_dir` |  "/var/tmp/archive" | 
`blackbox_exporter_configuration_modules` | * | check defaults/main.yml

```sh
mkdir -p /var/tmp/archive
cd /var/tmp/archive
wget https://github.com/prometheus/blackbox_exporter/releases/download/v0.18.0/blackbox_exporter-0.18.0.linux-amd64.tar.gz
```

Example Playbook
----------------

```yaml
---
- hosts: exporters
  gather_facts: true
  connection: ssh
  roles:
    - v98765_exporter_blackbox
```

License
-------

BSD
