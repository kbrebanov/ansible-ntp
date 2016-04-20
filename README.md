ntp
===

[![Ansible Role](https://img.shields.io/ansible/role/3307.svg)](https://galaxy.ansible.com/list#/roles/3307)

Installs and configures NTP.

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name        | Default                       | Description                                                                                                                                                                                        |
|:------------|:------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ntp_servers | [ "0.{{ ansible_distribution\ | lower }}.pool.ntp.org", "1.{{ ansible_distribution\|lower }}.pool.ntp.org", "2.{{ ansible_distribution\|lower }}.pool.ntp.org", "3.{{ ansible_distribution\|lower }}.pool.ntp.org" ] | NTP servers |

Dependencies
------------

None

Example Playbook
----------------

Install and configure NTP
```yaml
- hosts: all
  roles:
    - kbrebanov.ntp
```

Install and configure NTP specifying a NTP server
```yaml
- hosts: all
  vars:
    ntp_servers:
      - 0.pool.ntp.org
  roles:
    - kbrebanov.ntp
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
