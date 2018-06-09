Ansible Role: Pacemaker
=========

A simple Ansible role for setting up 2 node pacemaker cluster with a shared virtual IP Address

Requirements
------------

None.

Role Variables
--------------

See the `defaults/main.yml`

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: linux_routers
      roles:
        - role: rubentsirunyan.pacemaker
          vars:
            pcs_cluster_interface: eth1
            pcs_primary_address: 192.168.50.11
            pcs_secondary_address: 192.168.50.12
            pcs_cluster_name: myhacluster
            pcs_virtual_ip: 192.168.50.100
            pcs_disable_stonith: true

License
-------

BSD

Author Information
------------------

This role is created by Ruben Tsirunyan https://github.com/rubentsirunyan