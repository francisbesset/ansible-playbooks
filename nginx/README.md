nginx
=====

This playbook install the nginx package.

## Vars

* **delete_defaul_vhost**: Delete or not default vhost
    * Type: Boolean
    * Default: false
* **user**:
    * Type: String
    * Default: www-data
* **worker_processes**:
    * Type: Integer
    * Default: $ansible_processor_count
* **pid**:
    * Type: String
    * Default: /var/run/nginx.pid
* **worker_connections**:
    * Type: Integer
    * Default: 768

## Usage

``` bash
$ ansible-playbook nginx.yml -uroot
```
