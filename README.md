ntp
===

Installs and configures NTP.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

    # NTP servers
    ntp_servers:
      - 0.ubuntu.pool.ntp.org
      - 1.ubuntu.pool.ntp.org
      - 2.ubuntu.pool.ntp.org
      - 3.ubuntu.pool.ntp.org

    # NTP drift file
    ntp_driftfile: /var/lib/ntp/ntp.drift

Dependencies
------------

- selinux (CentOS)

Example Playbook
----------------

1) Install and configure NTP

    - hosts: all
      roles:
         - { role: selinux, when: ansible_distribution == "CentOS" }
         - { role: ntp }

2) Install and configure NTP specifying a NTP server

    - hosts: all
      roles:
         - { role: selinux, when: ansible_distribution == "CentOS" }
         - { role: ntp, ntp_servers: ['0.centos.pool.ntp.org'] }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
