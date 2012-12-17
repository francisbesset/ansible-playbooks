Python
======

These playbooks install different python tools.

## apt

The apt playbook install python-apt to use the `apt` ansible module on remote servers.
It is recommended to launch first.

### Usage

``` bash
$ ansible-playbook apt.yml -uroot
```

## mysqldb

The mysqldb playbook install python-mysqldb to use `mysql_db` and `mysql_user` ansible modules on remote servers.

### Usage

``` bash
$ ansible-playbook mysqldb.yml -uroot
```
