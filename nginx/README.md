nginx
=====

## nginx

This playbook install the nginx package.

### Vars

* **delete_default_vhost**: Delete or not default vhost
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

### Usage

``` bash
$ ansible-playbook nginx.yml -uroot
```

## vhost-redirect

This playbook add a simple redirect vhost for nginx.

### Vars

* **name**: The vhost name
    * Type: String
    * Default: redirect_$server_name
* **listen**:
    * Type: String
    * Default: *:80
* **server_name**: The server domain name
    * Type: String
    * Default: example.org
* **redirect_url**: The redirect URL
    * Type: String
    * Default: http://www.$server_name
