MySQL
=====

This playbook install the mysql-server package.

## Warning

If you use this playbook, it is highly recommended to set the `mysql_root_password` variable or launch manualy `mysql_secure_installation` command to:

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
  **mysql_root_password**: The password for the root user
    * Type: String
    * Default: Null

## Example usage

``` bash
$ ansible-playbook mysql.yml -uroot --extra-vars "mysql_root_password=TheUserRootPassword"
```
