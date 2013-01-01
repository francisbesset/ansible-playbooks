Memcached
=========

This playbook install memcached

## Vars

* **listen**:
  * Type: String
  * Default: 127.0.0.1
* **port**: The port which memcached deamon listen
  * Type: Integer
  * Default: 11211
* **user**: The user who launch the memcached deamon
  * Type: String
  * Default: nobody
* **memory**: The maximum memory used (in Mb)
  * Type: Integer
  * Default: 64
* **max_connections**: The maximum silmutaneous connections
  * Type: Integer
  * Default: 1024

## Usage

``` bash
$ ansible-playbook memcached.yml -uroot --extra-vars "listen=127.0.0.1 port=11211 user=nobody memory=64 max_connections=1024"
```
