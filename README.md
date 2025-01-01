Ansible Role: Telegraf
=========

Installs Telegraf on RHEL/CentOS, Debian/Ubuntu & OpenSUSE Servers

Requirements
------------

There are no pre-requisites for this role

Role Variables
--------------

See: `defaults/main.yml`

	REMOTE_IP: "monitoring.example.com"
The remote InfluxDB address

	REMOTE_DATABASE: "servers"
The remote InfluxDB Database Name

	REMOTE_USERNAME: "servers"
The remote InfluxDB Username

	REMOTE_PASSWORD: "password"
The remote InfluxDB Password

  SATELLITE_SUBSCRIPTION: true/false
Don't install from public repository on RHEL if this variable is present.

Dependencies
------------

There are no dependencies for this role.

Example Playbook
----------------

```yaml
- hosts: telegraf
  become: true

  vars:
    REMOTE_IP: "monitoring.example.com"
    REMOTE_DATABASE: "servers"
    REMOTE_USERNAME: "servers"
    REMOTE_PASSWORD: "password"

  roles:
    - role: jamdoog.telegraf
```

License
-------

BSD

Author Information
------------------

This role was created by James Ledger, I write about things on https://jamesledger.net

