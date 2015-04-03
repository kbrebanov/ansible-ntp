ntp
===

Installs and configures NTP.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name        | Default                                                                    | Description |
|-------------|----------------------------------------------------------------------------|-------------|
| ntp_servers | [ "0.pool.ntp.org", "1.pool.ntp.org", "2.pool.ntp.org", "3.pool.ntp.org" ] | NTP servers |

Dependencies
------------

CentOS:
  - kbrebanov.selinux

Example Playbook
----------------

Install and configure NTP
```
- hosts: all
  roles:
    - { role: kbrebanov.ntp }
```

Install and configure NTP specifying a NTP server
```
- hosts: all
  roles:
    - { role: kbrebanov.ntp, ntp_servers: ["0.centos.pool.ntp.org"] }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
