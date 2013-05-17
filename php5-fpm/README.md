PHP5
====

These playbooks install php5 tools.

## fpm

The fpm playbook install php5-fpm.

### Vars

* **delete_default_pool**: Delete or not the default pool (named "www")
    * Type: Boolean
    * Default: false

### Usage

``` bash
$ ansible-playbook fpm.yml -uroot
```

## fpm-pool

The fpm-pool add a fpm pool.

### Vars

* **name**: The name of pool
    * Type: String
    * Default: www
* **user**: The user of process
    * Type: String
    * Default: www-data
* **group**: The group of process
    * Type: String
    * Default: www-data
* **listen**: The socket or IP Address (with port)
    * Type: String
    * Default: /var/run/php5-fpm.sock
* **listen_allowed_clients**: List of ipv4 addresses of FastCGI clients which are allowed to connect. The IP must be seperated by comma
    * Type: String
    * Default: 127.0.0.1
* **pm_type**: The type of pool
    * Type: String
    * Default: dynamic
    * Possible values: static, dynamic, ondemand
* **pm_max_children**:
    * Type: Integer
    * Default: 5
* **pm_start_servers**:
    * Type: Integer
    * Default: 2
* **pm_min_spare_servers**:
    * Type: Integer
    * Default: 1
* **pm_max_spare_servers**:
    * Type: Integer
    * Default: 3
* **pm_process_idle_timeout**:
    * Type: String
    * Default: 10s
* **pm_max_requests**:
    * Type: Integer
    * Default: 500
* **pm_flag**:
    * Type: Array
    * Default: null
* **pm_admin_flag**:
    * Type: Array
    * Default: null
* **pm_admin_value**:
    * Type: Array
    * Default: null

### Usage

``` bash
$ ansible-playbook fpm-pool.yml -uroot
```

