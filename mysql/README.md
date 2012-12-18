MySQL
=====

This playbook install the mysql-server package.

## Warning

If you use this playbook, it is highly recommended to launch manualy `mysql_secure_installation` to:

* change the empty user root password
* disable root login remotely
* remove anonymous users
* remove `test` databases and access to it
* reload privilege tables

## Vars

* **mysqd**: Options for mysqld
    * Type: Array
    * Default:
        * bind_address: 127.0.0.1
        * key_buffer: 16M

## Example usage

``` bash
$ ansible-playbook mysql.yml -uroot
```
