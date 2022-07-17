Ansible Role: Telegraf
=========

Installs Telegraf on RHEL/CentOS, Debian/Ubuntu & OpenSUSE Servers

Requirements
------------

There are no pre-requisites for this role

Role Variables
--------------

See: `defaults/main.yml`

	REMOTE_IP: "http://192.168.200.1"
The remote InfluxDB address

	REMOTE_DATABASE: "servers"
The remote InfluxDB Database Name

	REMOTE_USERNAME: "servers"
The remote InfluxDB Username

	REMOTE_PASSWORD: "password"
The remote InfluxDB Password

  TEMPLATE: "telegraf.conf"
The template file you would like to deploy. This should represent a valid telegraf configuration file, with modifications for the above variables. 

Dependencies
------------

There are no dependencies for this role.

Example Playbook
----------------

```yaml
- hosts: telegraf
  become: true

  vars:
    REMOTE_IP: "https://192.168.50.1:8086"
    REMOTE_DATABASE: "servers"
    REMOTE_USERNAME: "servers"
    REMOTE_PASSWORD: "password"
    TEMPLATE: "telegraf.conf"

  roles:
    - role: jamdoog.telegraf
```

License
-------

BSD

Author Information
------------------

This role was created by James Ledger, I write about things on https://jamesledger.net

