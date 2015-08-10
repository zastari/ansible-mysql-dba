MySQL DBA Topologies
====================

This playbook installs MySQL, configures replication topologies, and installs HA replication tools. Currently, only  RHEL/CentOS 5, 6, and 7 are supported. The following operations are supported:

Version Installations:
 * Percona Server 5.6
 * Percona Server 5.5
 * MySQL 5.6
 * MySQL 5.5
 * MariaDB 10.0
 * MariaDB 5.5

Topologies:
 * Master/Slave (1 or many slaves)
 * Master/Master

HA Management Tools:
 * MySQL MMM (http://mysql-mmm.org/doku.php)

Role Variables
--------------

Servers that will be in a replication topology must have the following parameters assigned to ensure that replication does not break due to conflicts:
 * name
 * server_id
 * repl_parent

MySQL version control is provided through the mysql_version variable. Valid values are mysql_55, mysql_56, ps_55, ps_56, mariadb_55, mariadb_100.

Roadmap
-------

The following functionality is planned but not yet implemented
 * Installing older versions of the available releases
 * Installing to a sandbox instance using dbsake sandbox
 * MySQL MasterHA
 * Galera

License
-------

BSD

Author Information
------------------

Tyler Mitchell
