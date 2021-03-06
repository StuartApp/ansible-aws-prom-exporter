AWS Prometheus Exporter (aka AWS Prom Exporter)
=========

This role installs and configures [aws-prom-exporter](https://github.com/StuartApp/ansible-aws-prom-exporter)

Requirements
------------

None

Role Variables
--------------

```yaml
---

# Repository from where to install aws-prom-exporter
aws_prom_exporter_repo_url: git+https://git@github.com/StuartApp/aws-prom-exporter

# Version to install
aws_prom_exporter_version: v0.2

# Configuration settings as specified in aws-prom-exporter repository README
# If empty, aws-prom-exporter defaults will be used (and an empty config.yaml file will be created)
aws_prom_exporter_config: ""

# Where to create the configuration file
aws_prom_exporter_config_file_dir: /etc/aws-prom-exporter

# Status of the service after installation
aws_prom_exporter_svc_state: started

# Wether enable or not the service (to start it after reboot)
aws_prom_exporter_svc_enabled: true
```

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: StuartApp.aws-prom-exporter,  aws_prom_exporter_version: "v0.2" }

License
-------

GPL-3

Author Information
------------------

Jordi Clariana
