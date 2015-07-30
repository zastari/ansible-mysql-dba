MySQL DBA Ansible Plays
=======================

These plays are designed to deploy common replication topologies with best
practices for secure, high-throughput environments. Currently, master/slave
replication with an arbitrarily large number of slaves is supported. 

These scripts are designed for RHEL/CentOS 5 or 6. RHEL 7 support is planned.
There is no plan to provide Debian or other distro support at this time. Once
complete, the following plays will be available:

Version Installations:
 * Percona Server 5.6
 * Percona Server 5.5
 * MySQL 5.7
 * MySQL 5.6
 * MySQL 5.5
 * MariaDB 10.0

Topologies:
 * Master/Slave (1 or many slaves)
 * Master/Master
 * MMM ( http://mysql-mmm.org/doku.php )
 * MasterHA ( https://code.google.com/p/mysql-master-ha/ )
 * Galera

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

name and server_id host variables must be defined in the inventory file.
Failure to do so will result in server_id conflicts and cause replication
errors.

Depending on the replication topology, different group variables will be
configured in the group_vars files corresponding to the type of topology
being deployed. Full specifications are available in these files:

      group_vars/mysql
      group_vars/mysql_slave

Examples
--------

1) Create Master/Slave replication:

      cp hosts.example hosts
      ansible-playbook -i hosts master-slave.yml

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Tyler Mitchell
