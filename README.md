Ansible
=======

My ansible playbooks.

## Usage

``` yaml
---
  - hosts: webservers

  - include: python/apt.yml
  - include: apt/dotdeb.yml
    vars:
      with_php54: false

  - include: iptables/persistent.yml
    vars:
      iptables_file_rules: ../../an_iptables_file_rules

  - include: python/mysqldb.yml
  - include: mysql/mysql.yml
    vars:
      mysql_root_password: TheUserRootPassword
      mysqld:
        bind_address: 127.0.0.1
        key_buffer: 16M
        max_connection: 100
        # skip archive storage engine
        skip-archive: ~
        # you can add other key/value

  - include: php5/fpm.yml
    vars:
      delete_default_pool: true
  - include: php5/fpm-pool.yml
    vars:
      name: foo
      listen: /var/run/php5-fpm-foo.sock
      pm_process_idle_timeout: 20s
      pm_max_requests: 100
      php_flag:
        display_errors: off
        # you can add other key/value
      php_admin_flag:
        log_errors: on
        # you can add other key/value
      php_admin_value:
        memory_limit: 64M
        # you can add other key/value
  - include: php5/fpm-pool.yml
    vars:
      name: bar
      listen: /var/run/php5-fpm-bar.sock

  - include: nginx/nginx.yml
    vars:
      delete_default_vhost: true
  - include: nginx/vhost-redirect.yml
    vars:
      name: redirect_$server_name
      listen: "*:80"
      server_name: example.org
      redirect_url: http://www.$server_name

  - include: memcached/memcached.yml
    vars:
      listen: 127.0.0.1
      listen: 11211
      memory: 64
      max_connections: 1024

  - include: swap/swappiness.yml
    vars:
      swappiness: 60
```
