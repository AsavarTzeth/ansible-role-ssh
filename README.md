[![Build Status](https://travis-ci.org/AsavarTzeth/ansible-role-ssh.svg?branch=master)](https://travis-ci.org/AsavarTzeth/ansible-role-ssh)

Ansible SSH Role - ansible-role-ssh
===================================

**Ansible role that configures ssh and enables systemd socket activation.**

Requirements
------------

This role was developed and tested on Ansible 2.2.0 and higher.
It may work on lower versions but that is currently unsupported.

Role Variables
--------------

    ssh_port: (default: 22)  # The tcp port the socket will listen on
    ssh_socket_bind_device:  # The interface the socket will bind to
    ssh_users:               # Equivalent to sshd_config(5) AllowUsers

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
        - role: AsavarTzeth.ssh
          ssh_port: 22
          ssh_socket_bind_device: eth0
          ssh_users: foobar1 foobar2

License
-------

BSD-2-Clause

Author Information
------------------

Patrik Nilsson
