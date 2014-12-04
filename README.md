ntp
===

Installs and configures NTP.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

    # NTP servers
    ntp_server_0: 0.centos.pool.ntp.org
    ntp_server_1: 1.centos.pool.ntp.org
    ntp_server_2: 2.centos.pool.ntp.org
    ntp_server_3: 3.centos.pool.ntp.org

Dependencies
------------

- selinux

Example Playbook
----------------

1) Install and configure NTP

    - hosts: all
      roles:
         - { role: ntp }

2) Install and configure NTP specifying a NTP server

    - hosts: all
      roles:
         - { role: ntp, ntp_server_0: 127.0.0.1 }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
